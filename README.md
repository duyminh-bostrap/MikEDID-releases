# MikEDID releases

Download page for **MikEDID**: lock the EDID of projectors, LED processors and virtual outputs, so a show machine keeps its display layout through hot-plugs, switcher cuts and reboots.

This repo only holds the installers. Get the latest one from the [Releases page](https://github.com/duyminh-bostrap/MikEDID-releases/releases/latest).

## Files in each release

| File | What it is |
|---|---|
| `MikEDID.exe` | Windows 64-bit, portable. Nothing to install |
| `SHA256SUMS.txt` | SHA-256 of every file in the release |

## Verify your download

```powershell
Get-FileHash .\MikEDID.exe -Algorithm SHA256
```

The hash must match the line for `MikEDID.exe` in `SHA256SUMS.txt`.

## First launch (Windows)

1. Start `MikEDID.exe`. The build is **not code-signed**, so SmartScreen may warn: click **More info**, then **Run anyway**.
2. The window uses the Microsoft Edge WebView2 runtime. It is built into Windows 11. On Windows 10, install it from Microsoft if the window stays blank.
3. Locks that write the registry override need **Run as administrator**.
4. To rehearse without touching any hardware, run `MikEDID.exe --demo`.

## Notes

- NVIDIA GPU locks (RTX and Quadro) last for the current boot. Switch on **START WITH OS · PERSIST LOCK** so the background daemon re-applies them at login.
- The app works fully offline.
- macOS and Linux builds are not published here yet.

## Docs and support

This repo hosts files only. TODO(owner): add the store page URL (tutorial, docs) and a support contact.

Copyright (c) MikMap. All rights reserved. Use MikEDID on show machines at your own risk and keep a known-good configuration to roll back to.
