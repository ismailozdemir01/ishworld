# THE ISHWORLD Downloads

This repository is the **public distribution surface** for ISHWORLD.

Enterprise source code, internal tests, private integrations, build credentials and secrets remain in the private Enterprise repository.

## Current validated release — v7.1.5

The v7.1.5 distribution was produced by the private Enterprise CI pipeline and passed source verification, automated validation, native builds, application health checks, Windows installer checks, Windows uninstall verification and checksum generation before publication.

Available from the public GitHub Release:

- Windows x64 executable: `ISHWORLD-7.1.5-Windows-x64.exe`
- Windows x64 installer: `ISHWORLD-7.1.5-Windows-x64-Setup.exe`
- Linux x64 executable: `ISHWORLD-7.1.5-linux-x64`
- SHA-256 manifest: `SHA256SUMS.txt`

No Enterprise source archive is distributed as a release artifact.

## Installation

For Windows, the recommended distribution method is the x64 installer. The standalone executable is available for portable/manual operation.

For Linux x64, download the executable, make it executable, and run it from the directory where you want the local runtime to operate.

See [`INSTALLATION.md`](INSTALLATION.md) for platform-specific steps and [`USER_GUIDE.md`](USER_GUIDE.md) for first-run and operational usage.

## Integrity

Always download the release assets from the official GitHub Release and verify the SHA-256 value against `SHA256SUMS.txt` before deployment in a controlled environment.

## Release policy

The private Enterprise repository performs source verification, automated tests, native builds, installer install/health/uninstall checks and checksum generation. Only the resulting validated distribution artifacts are copied to this public repository's GitHub Release.

A release is not advertised as validated until the complete publication pipeline succeeds.
