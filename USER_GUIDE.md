# THE ISHWORLD — User Guide

## v7.1.5

## 1. What you receive

The public distribution contains validated runtime binaries only. Enterprise source code, private integrations, internal tests and secrets are not part of the public distribution.

## 2. First run

Install or launch the platform using the procedure in [`INSTALLATION.md`](INSTALLATION.md).

After startup, use the application's local control surface and runtime behavior as provided by the release. Do not assume that absent world content is automatically generated: ISHWORLD intentionally reports missing production configuration explicitly.

## 3. Core operating model

ISHWORLD is a server-authoritative persistent-world runtime. Its production runtime is built around explicit domain state, an event journal, persistence, player identity, deterministic simulation and renderer-neutral contracts.

The current runtime scope includes world/event state, spatial simulation and discovery, cities and economy, world stability, NPC memory/life/society, factions and diplomacy, player progression and knowledge, dynamic story/investigation, validated GLB/GLTF asset contracts, animation/locomotion contracts, fixed-timestep simulation, collision/grounding, camera/render-frame contracts and deterministic navigation.

## 4. Production content

Production content must be explicitly registered/configured. The runtime does not silently create a seed world, fabricated map, fake mesh, fake texture, fake animation, fake weather or fake navigation graph.

When a required production dependency is absent, use the reported `NOT_CONFIGURED`, `UNKNOWN`, `UNAVAILABLE` or domain error state to identify what must be configured.

## 5. Real 3D assets

The runtime validates local `.glb` / `.gltf` assets through explicit contracts. A photorealistic human mesh is not fabricated by the runtime. Register a real production asset before expecting a renderable character.

## 6. Navigation

Navigation is content-driven. Real nodes and edges must be registered for the relevant region before pathfinding can operate for that region. Cross-region routing requires an explicit regional navigation connector.

## 7. Operations checklist

Before a production deployment:

- Verify the release asset checksum.
- Use the Windows installer for managed Windows deployment where appropriate.
- Keep the runtime on a controlled host and network boundary.
- Register real production world/content assets instead of relying on generated substitutes.
- Confirm required configuration is present and that the runtime is not reporting `NOT_CONFIGURED` or `UNAVAILABLE` for required services.
- Keep Enterprise source and secrets out of customer/public distribution locations.

## 8. Upgrade procedure

1. Back up any deployment-specific persistent data according to your operational policy.
2. Download the new validated release.
3. Verify its SHA-256 checksum.
4. Stop the currently running instance.
5. Install the new Windows release or replace the Linux executable according to the release instructions.
6. Start the new version and perform the application's normal health/operational checks.
7. Review configuration and content status before returning the deployment to service.

## 9. Uninstall

On Windows, use the normal Windows uninstall mechanism. v7.1.5's release pipeline includes an installer/uninstaller validation step.

On Linux, stop the running process and remove the executable and any deployment-specific files according to the host's operational policy.

## 10. Security boundary

The public repository is a distribution surface, not the Enterprise source repository. Do not place credentials, private integration configuration, customer secrets or internal build material in the public repository.

For security-sensitive deployment decisions, apply the organization's own host, network, identity, backup and access-control policies in addition to the application's runtime controls.
