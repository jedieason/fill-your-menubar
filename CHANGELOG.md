# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [2.0.8] - 2026-09-29

### Added
- **Automatic & Manual Update Checker:** Integrated GitHub Releases check with direct update notifications, release notes, and download links in Settings and Menu Bar menu.
- **Rebrand:** Renamed application to **Fill Your Menubar** with slogan *"Bring your menubar back alive."*

### Fixed
- **Palette Editor Crash:** Fixed fatal runtime trap (`SIGTRAP` / `Index out of range`) when removing color swatches in the palette editor by guarding bounds in `Binding` getters, setters, and removal actions.
- **Spread Entrance Stability:** Resolved screen contamination checks during Space switching to ensure seamless 0.32s entrance animations without flashing.
- **Full Screen Menu Preservation:** Restored missing app-owned menu titles in fullscreen spaces across secondary displays.
