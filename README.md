# FrameTune

Finds the best NVIDIA settings for **your** PC and applies them in one click.

It detects your graphics card automatically (every GeForce, RTX, TITAN, MX and Quadro/RTX workstation card from the GTX 400 series to the RTX 50 series, desktop and laptop), reads your monitor and Windows setup, and recommends settings for the goal you pick.

## Features

- **Auto-detects your card**: model, generation, VRAM, driver version and age, PCIe link.
- **Three goals**: Max FPS, Balanced and Max Quality.
- **Driver settings**: the same options as NVIDIA Control Panel → Manage 3D settings, shown as current vs. recommended, with a plain-English reason for each one.
- **Windows 10 and 11 checks**: GPU scheduling, Game Mode, background recording, windowed-game optimizations, power plan, refresh rate, monitor cable and driver age.
- **One-click Optimize** and a full **Undo**. Everything is backed up before it changes.
- **In-game settings guide** for your card and resolution: quality preset, textures, DLSS, Frame Generation, Reflex, ray tracing and V-Sync.
- **Live monitor** of usage, temperature, clocks, power, VRAM and fan, with one minute of history.
- Automatic updates.

It never overclocks, flashes firmware or edits game files.

## Requirements

- Windows 10 (version 2004 or newer) or Windows 11, 64-bit.
- An NVIDIA graphics card with its driver installed.

## Install

Download `FrameTune-Setup-<version>.exe` from [Releases](https://github.com/AntiLegend93/FrameTune/releases) and run it. No admin rights are needed to install. Windows asks for permission only when driver settings are changed.

## Building

1. Install Visual Studio 2022 with the **.NET desktop development** and **Windows App SDK C# templates** workloads, plus [Inno Setup 6](https://jrsoftware.org/isdl.php).
2. Run `build\build-release.bat`.
3. The app is in `dist\FrameTune\` and the installer is `dist\FrameTune-Setup-<version>.exe`.

To release an update, raise the version in `Directory.Build.props` and `version.txt`, build, and attach the Setup.exe to a GitHub release tagged `v<version>`.

---

FrameTune is an independent app and isn't made or endorsed by NVIDIA. NVIDIA, GeForce, RTX, G-SYNC, DLSS and Reflex are trademarks of NVIDIA Corporation.
