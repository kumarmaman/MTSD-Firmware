# MTSD Firmware

This public repository distributes signed, binary-only OTA releases for MTSD devices. The firmware source remains in a separate private repository.

Each GitHub release contains:

- `firmware.bin` — credential-free ESP32 application image
- `manifest.json` — version, download URL, image size, SHA-256 digest, and ECDSA signature

The device accepts an update only when the embedded public key validates the manifest and the downloaded image matches both its declared size and SHA-256 digest. No GitHub access token or backend bootstrap credential is stored in these public artifacts.

Release assets are generated automatically from the private source repository. Do not upload manually built bootstrap firmware here.
