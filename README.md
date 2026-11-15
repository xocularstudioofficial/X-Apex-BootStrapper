<div align="center">

<img src="banner.jpg" alt="X-Ocular Studio Banner" width="100%">
<br><br>

<h1>X-APEX BOOTSTRAPPER</h1>

**A proprietary C++20 / Win32 alternative launcher and client configuration utility for Roblox on Windows, developed by X-Ocular Studio.**

![Platform](https://img.shields.io/badge/Platform-Windows%2010%2F11%20(x64)-FF6B00?style=for-the-badge&logo=windows&logoColor=white)
![Language](https://img.shields.io/badge/Built%20With-C%2B%2B20%20%2F%20Win32-1A1A1A?style=for-the-badge&logo=cplusplus&logoColor=FF6B00)
![Status](https://img.shields.io/badge/Release-v0.3.0-FF6B00?style=for-the-badge)
![License](https://img.shields.io/badge/License-All%20Rights%20Reserved-red?style=for-the-badge)

</div>

---

## Overview

**X-Apex Bootstrapper** is a native Windows desktop launcher and configuration utility built with C++20, the Win32 API, and Microsoft Edge WebView2. It is designed to manage local Roblox client settings, apply local asset overrides, browse public game servers, and monitor basic system resource usage from a single interface.

> **Disclaimer:** X-Apex Bootstrapper is an independent third-party utility and is not affiliated with, endorsed, or officially supported by Roblox Corporation. Use of third-party launchers and client configuration tools is at your own discretion and risk.

---

## Documented Features

- **Local FastFlags & Configuration Management:**
  - Provides a table editor and raw JSON editor for managing local `ClientAppSettings.json` profiles.
  - Includes optional presets for common rendering and graphics flags (such as Direct3D 11 / Vulkan selection, lighting modes, and MSAA).
  - Allows editing local `GlobalBasicSettings_13.xml` parameters (target framerate, fullscreen state, audio volume, and mouse sensitivity), with an optional `Read-Only` file attribute toggle.
- **Local Client Asset Overrides:**
  - Supports replacing local client asset files on disk, including custom fonts (`.ttf`, `.otf`), audio files, mouse cursors, and Shift Lock icons.
- **Public Server Browser & Session Launching:**
  - Queries publicly available server instance data via Roblox web endpoints to display player counts, estimated latency, and server metrics.
  - Supports launching the official Roblox client into a selected `PlaceId` / `JobId` or choosing a server based on player count or latency filters.
- **System Resource Telemetry & Process Options:**
  - Displays real-time CPU usage, system RAM usage, and `RobloxPlayerBeta.exe` memory consumption.
  - Includes optional Windows API controls for process scheduling priority, CPU core affinity, Windows 11 power-throttling states (`PROCESS_POWER_THROTTLING_EXECUTION_SPEED`), multimedia timer resolution (`timeBeginPeriod`), and working-set memory trimming (`EmptyWorkingSet`).
  - Includes an option to terminate `RobloxCrashHandler.exe` in the background.
- **Win32 Overlay Window (`Insert` Hotkey):**
  - Displays an Always-on-Top translucent Win32 overlay window showing basic system telemetry and quick-launch controls without switching windows.
- **Multi-Instance Session Option (`ROBLOX_singletonMutex`):**
  - Attempts to close or manage the `ROBLOX_singletonMutex` handle to allow launching multiple client instances simultaneously. *(Note: Running multiple Roblox clients simultaneously is not officially supported by Roblox.)*
- **Additional Utilities:**
  - Discord Rich Presence integration for displaying active game sessions.
  - JSON configuration export and import.
  - Interface localization in English, Serbian, and German.

---

## Installation

1. Open the **[Releases](../../releases)** page of this repository.
2. Download the official installer package (`X-Apex_Installer_v0.3.0.exe`) exclusively from the **Assets** section of the latest release.
3. Run the installer and follow the on-screen setup instructions. Existing user profiles and local configuration files are preserved during updates.

---

## Security Notices & Known Limitations

- **Unsigned Binary:** The distributed executable and installer are currently **not digitally signed** with a commercial Code Signing certificate. Windows Defender SmartScreen or third-party antivirus software may display a warning for unrecognized publishers. Only download releases directly from this official repository and verify file checksums (SHA-256) when provided in the release notes.
- **Closed-Source Distribution:** Because the C++ source code is proprietary and not publicly hosted in this repository, third parties cannot independently audit the compiled binaries.
- **Third-Party Software Policy:** Roblox does not officially support third-party bootstrappers, multi-instance tools, or external process modifications. Future Roblox client or anti-cheat updates may break compatibility or restrict the use of external utilities.
- **Process & File Modifications:** Features that alter process priority, terminate `RobloxCrashHandler.exe`, lock configuration files as `Read-Only`, or manage `ROBLOX_singletonMutex` interact directly with Windows processes and local client files, which may cause client instability or conflicts with security software.

---

## Support & Bug Reports

- **Diagnostic Logs:** You can access local diagnostic logs inside the application via **Settings / Bootstrapper → Open Logs**.
- **Issue Tracker:** Report bugs or compatibility issues in the **[Issues](../../issues)** tab of this repository.

---

## License & Copyright

© 2026 **X-Ocular Studio**. **All Rights Reserved.**

This software is **proprietary (closed-source)** software, not open-source. No license is granted to copy, modify, distribute, decompile, reverse-engineer, or create derivative works from the binaries, installers, branding, or associated assets without prior written permission from **X-Ocular Studio**.
