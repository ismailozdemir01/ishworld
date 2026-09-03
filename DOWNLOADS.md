# THE ISHWORLD — Downloads

**A World That Remembers. Your choices become history.**

This repository is the **public distribution surface** for ISHWORLD.

- Proprietary Enterprise source code remains private.
- Internal tests, private integrations, build credentials and secrets are not distributed.
- Public releases contain validated runtime binaries and release verification files.

## Current release — v8.0.0

The v8.0.0 binaries were produced by the private Enterprise release pipeline and passed source verification, automated tests, native builds, application smoke checks, Windows installer/install/uninstall validation and checksum generation before public publication.

### Windows x64

- `ISHWORLD-8.0.0-Windows-x64-Setup.exe` — recommended installer
- `ISHWORLD-8.0.0-Windows-x64.exe` — portable executable

### Linux x64

- `ISHWORLD-8.0.0-linux-x64` — native Linux executable

### Integrity

- `SHA256SUMS.txt`
- `SHA256SUMS-linux-x64.txt`

Download the binaries only from the official release page and verify the SHA-256 checksum before deployment.

## Distribution boundary

The public repository is intentionally source-free. GitHub may display automatically generated **Source code (zip)** / **Source code (tar.gz)** entries for a release; these archives contain only the files present in the public distribution commit, not the proprietary Enterprise source.

Android/iOS native packages are not advertised as released until real native builds and platform validation are completed.

## Installation

See [`INSTALLATION.md`](INSTALLATION.md) for Windows and Linux installation and verification steps. See [`USER_GUIDE.md`](USER_GUIDE.md) for operating guidance.
