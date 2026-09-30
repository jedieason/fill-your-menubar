# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [2.0.10] - 2026-09-30

### Added
- **Gatekeeper First-Launch Onboarding:** Step-by-step visual documentation for opening Fill Your Menubar seamlessly on macOS.
- **Active Display Switching:** Dynamic tracking (`DisplaySelection.activeID`) that automatically shifts the menu bar overlay to the active monitor based on window focus, foremost app, and cursor activity when single-display mode is selected.
- **Comprehensive Debug & Diagnostics Monitor:** Interactive live monitoring dashboard recording real-time color palettes, window layering levels (Layer 24 tint vs Layer 26 composite), safe area top insets, and instant one-click "Copy Log for AI" diagnostics report.

### Improved
- **ScreenCaptureKit Lifecycle & Disconnect Recovery:** Robust transient error backoff and stream recovery for ScreenCaptureKit disconnects (-3802 through -3821), display attachments, and Space switches.
- **Multi-Display Fullscreen Tracking:** Independent per-screen tracking (`fullscreenDisplays`) ensuring smooth transitions without clipping across multiple monitors.
- **Notch & Menu Bar Height Alignment:** Native WindowServer menu bar height matching across built-in MacBook Pro notch displays and external monitors.

## [2.0.9] - 2026-09-29

### Added
- **Display Selection Tracking:** Automatically identify and switch the active menu bar display.
- **Debug Monitor Card:** Diagnostics card in Settings and status item menu.

### Fixed
- **ScreenCaptureKit Stream Resilience:** Reconnect stream automatically on Space transitions and wake events.
- **Split-View Geometry Recognition:** Corrected fullscreen detection for split-screen Spaces.

## [2.0.8] - 2026-09-29

### Added
- **Automatic & Manual Update Checker:** Integrated GitHub Releases check with direct update notifications, release notes, and download links in Settings and Menu Bar menu.
- **Rebrand:** Renamed application to **Fill Your Menubar** with slogan *"Bring your menubar back alive."*

### Fixed
- **Palette Editor Crash:** Fixed fatal runtime trap (`SIGTRAP` / `Index out of range`) when removing color swatches in the palette editor by guarding bounds in `Binding` getters, setters, and removal actions.
- **Spread Entrance Stability:** Resolved screen contamination checks during Space switching to ensure seamless 0.32s entrance animations without flashing.
- **Full Screen Menu Preservation:** Restored missing app-owned menu titles in fullscreen spaces across secondary displays.
