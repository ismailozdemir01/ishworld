# THE ISHWORLD — Installation Guide

## v8.0.0

This guide covers the validated public distribution.

## Windows x64 — recommended

1. Open the `v8.0.0` release in the public repository.
2. Download `ISHWORLD-8.0.0-Windows-x64-Setup.exe`.
3. Verify its SHA-256 hash against `SHA256SUMS.txt`.
4. Run the installer and complete the installation.
5. Launch ISHWORLD from the installed application entry or executable.
6. Use the normal Windows uninstall mechanism when removing the application.

The v8.0.0 release pipeline validates native executable startup, installer operation, installed executable startup and uninstall cleanup.

### Portable Windows executable

`ISHWORLD-8.0.0-Windows-x64.exe` is available for portable/manual operation. Download it from the release, verify its SHA-256 hash, and launch it directly.

## Linux x64

1. Download `ISHWORLD-8.0.0-linux-x64` from the v8.0.0 release.
2. Verify its SHA-256 hash against the published manifest.
3. Grant execute permission:

```bash
chmod +x ISHWORLD-8.0.0-linux-x64
```

4. Start it:

```bash
./ISHWORLD-8.0.0-linux-x64
```

The v8.0.0 Linux build is smoke-tested by the release pipeline.

## Verification

### Windows PowerShell

```powershell
Get-FileHash .\ISHWORLD-8.0.0-Windows-x64-Setup.exe -Algorithm SHA256
```

### Linux

```bash
sha256sum ISHWORLD-8.0.0-linux-x64
```

Compare the result with `SHA256SUMS.txt` from the release.

## Distribution boundary

The public repository is intentionally source-free. The proprietary Enterprise source, private integrations, internal build material, signing credentials and secrets remain outside the public distribution.

GitHub automatically provides source-archive links for public release tags. Those archives contain the public distribution commit only; they do not expose the private Enterprise source.

## Production data rule

ISHWORLD does not silently manufacture production world data or assets. Missing production configuration/content is reported explicitly as `NOT_CONFIGURED`, `UNKNOWN`, `UNAVAILABLE` or a domain error.

## Troubleshooting

- If the application does not start, verify the downloaded file's SHA-256 hash first.
- If required production content is missing, inspect the reported configuration/domain status instead of expecting fabricated substitutes.
- For a clean Windows reinstall, uninstall the existing installation before installing the new release.
