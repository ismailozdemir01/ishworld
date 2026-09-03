# THE ISHWORLD — Installation Guide

## v7.1.5

This guide covers deployment of the validated public distribution.

## Windows x64 — recommended

1. Open the `v7.1.5` release in the public repository.
2. Download `ISHWORLD-7.1.5-Windows-x64-Setup.exe`.
3. Verify its SHA-256 hash against `SHA256SUMS.txt`.
4. Run the installer and complete the installation.
5. Launch ISHWORLD from the installed application entry or the installed executable.
6. When the application is no longer required, use the normal Windows uninstall entry.

The v7.1.5 release pipeline explicitly validates executable startup, installer operation and uninstall cleanup.

### Portable Windows executable

`ISHWORLD-7.1.5-Windows-x64.exe` can be used when an installer-based deployment is not desired. Download it from the release, verify its SHA-256 hash, and launch it directly.

## Linux x64

1. Download `ISHWORLD-7.1.5-linux-x64` from the v7.1.5 release.
2. Verify its SHA-256 hash against `SHA256SUMS.txt`.
3. Grant execute permission:

```bash
chmod +x ISHWORLD-7.1.5-linux-x64
```

4. Start it:

```bash
./ISHWORLD-7.1.5-linux-x64
```

The validated Linux build includes an application health smoke test in the release pipeline.

## Verification

The release contains a SHA-256 manifest. Do not treat a download as trusted solely because the filename is correct; compare the locally calculated hash with the published manifest.

### Windows PowerShell

```powershell
Get-FileHash .\ISHWORLD-7.1.5-Windows-x64-Setup.exe -Algorithm SHA256
```

### Linux

```bash
sha256sum ISHWORLD-7.1.5-linux-x64
```

## Network and configuration

The runtime is designed to operate locally and does not require an external API service for its core local control surface. The documented default local control surface is `127.0.0.1:8765` when running the Python/runtime form.

Do not expose a local control surface to an untrusted network without an explicitly configured deployment boundary and appropriate network controls.

## Production data rule

ISHWORLD does not silently manufacture production world data. Missing production configuration or content is represented explicitly as `NOT_CONFIGURED` or a domain error rather than substituted with fabricated assets or state.

## Troubleshooting

- If the application does not start, first verify that the downloaded file's SHA-256 matches the release manifest.
- If a required production asset or world configuration is missing, inspect the reported `NOT_CONFIGURED` or domain error instead of expecting automatic fake content.
- For a clean Windows reinstall, uninstall the existing installation before installing a new version.
