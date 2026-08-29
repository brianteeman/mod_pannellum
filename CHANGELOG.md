# Changelog

All notable changes to the Pannellum 360° Viewer module will be documented in this file.

## [1.0.1] - 2026-08-29

### Fixed

- **Critical: Multiple module instances** – Using two or more Pannellum modules on the same page caused a 500 error ("Cannot redeclare hexToRgba()"). The global PHP function has been converted to a scoped closure.
- **Auto-Load in Multi-Scene Mode** – The auto-load setting was ignored in multi-scene mode (always forced to "on"). It now respects the configured value.
- **Display options not applied** – Compass, auto-rotation speed, and auto-rotation delay settings had no effect because they were not passed to the Pannellum viewer.

### Added

- **Localized loading text** – The "Loading..." and "Click to Load Panorama" texts are now translatable via Joomla language files (German and English included).

### Changed

- Removed debug `console.log` statements from the frontend JavaScript for cleaner browser console output.

## [1.0.0] - 2026-03-29

### First Public Release

- **Single Panorama Mode** with optional hotspots and image description overlay
- **Multi-Scene Mode** for interactive virtual tours with linked panoramas
- **Visual Hotspot Editor** for placing hotspots by clicking in the panorama
- **Scene Link Hotspots** for navigation between panorama scenes
- **Info Point Hotspots** with rich HTML content support (filtered via Joomla safehtml)
- **Per-Scene Image Descriptions** with customizable position, font size, color, and opacity
- **Font Awesome Icon Support** for hotspots with adjustable color and size
- **Display Options:** configurable height (px/vh), drop shadow, compass, auto-rotation
- **Mobile Gyroscope Support** for device orientation control
- **Fullscreen Mode** with proper z-index management
- **Multilingual:** complete German (de-DE) and English (en-GB) language files
- **Joomla Update Server** via GitHub for automatic update notifications
- Compatible with Joomla 5.x and 6.x (PHP 8.1+)
