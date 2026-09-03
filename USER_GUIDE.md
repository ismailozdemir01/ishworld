# THE ISHWORLD — User Guide

## v8.0.0

## 1. What you receive

The public distribution contains validated runtime binaries. Proprietary Enterprise source code, private integrations, internal tests and secrets are not part of the public distribution.

## 2. First run

Install or launch ISHWORLD using [`INSTALLATION.md`](INSTALLATION.md).

After startup, use the application's native runtime and available control surface. Required production configuration and content are reported explicitly when unavailable.

## 3. Core operating model

ISHWORLD is a server-authoritative persistent-world runtime built around explicit domain state, an event journal, persistence, player identity, deterministic simulation and renderer-neutral contracts.

The runtime scope covers world/event state, spatial simulation and discovery, cities and economy, world stability, NPC memory/life/society, factions and diplomacy, player progression and knowledge, dynamic story/investigation, validated 3D asset contracts, animation/locomotion contracts, fixed-timestep simulation, collision/grounding, camera/render-frame contracts and deterministic navigation.

## 4. Production content

Production content must be explicitly registered/configured. The runtime does not silently substitute fabricated maps, meshes, textures, animations, weather or navigation graphs for missing production dependencies.

When a required dependency is absent, use the reported `NOT_CONFIGURED`, `UNKNOWN`, `UNAVAILABLE` or domain error state.

## 5. Real 3D assets

Real `.glb` / `.gltf` production assets are validated through explicit contracts. Production content should be registered before deployment where required by the runtime configuration.

## 6. Navigation

Navigation is content-driven. Real nodes and edges must be registered for the relevant region before pathfinding can operate there. Cross-region routing requires an explicit regional navigation connector.

## 7. Operations checklist

- Verify the release checksum.
- Use the Windows installer for managed deployment where appropriate.
- Keep the runtime within a controlled host/network boundary.
- Register real production world/content assets.
- Confirm required configuration is present.
- Keep Enterprise source, credentials and secrets out of public/customer distribution locations.

## 8. Upgrade procedure

1. Back up deployment-specific persistent data according to your operational policy.
2. Download the new validated release.
3. Verify its SHA-256 checksum.
4. Stop the current instance.
5. Install the new Windows release or replace the Linux executable according to the installation guide.
6. Start the new version and perform normal health/operational checks.
7. Review configuration and content status before returning the deployment to service.

## 9. Uninstall

On Windows, use the normal Windows uninstall mechanism. The v8.0.0 release pipeline validates installer/uninstaller behavior.

On Linux, stop the running process and remove the executable and deployment-specific files according to host policy.

## 10. Security boundary

The public repository is a player-facing distribution surface, not the Enterprise source repository. Do not place credentials, private integration configuration, customer secrets or internal build material in it.
