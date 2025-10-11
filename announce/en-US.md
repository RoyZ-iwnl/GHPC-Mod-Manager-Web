# Welcome to GHPC Mod Manager

## Announcement

### 2025-10-11

- v1.1.1 stable release is now available with Steam auto-discovery and translation UX upgrades. See the [changelog](#v111) below for details.

### 2025-10-09

- v1.1.1-beta.1 beta version is now available with BepInEx detection and UI enhancements. See the [changelog](#v111-beta1) below for details.

### 2025-10-05

- v1.1.0 with polish translation UX and update flows with smarter downloads is now available! See the [changelog](#v110) below for details.
- Add support for Mod: Customizer Unrestricted

### 2025-10-01

- v1.1.0-beta.1 beta version is now available with the in-app updater and translation upgrades. See the [changelog](#v110-beta1) below for details.
- Add support for Mod: Stabilized BMP-1

### 2025-09-23

- v1.0.1 Version has been released! Fixed several minor issues, details are in the [changelog](#v101) below.

### 2025-09-04

- v1.0.0 Version has been released! Looking forward to your feedback and suggestions! If you encounter conflicts between mods, you can also report them so that we can add conflict detection.<br>
[DOWNLOAD HERE](https://github.com/RoyZ-iwnl/GHPC-Mod-Manager/releases)

### 2025-09-03

- GHPC version 20250902 has been released. Some mods may not be compatible. Please install or update accordingly.

## Changelog

### v1.1.1

#### feat: Release version 1.1.1 with Steam auto-discovery and translation UX upgrades
  - Provide SteamGameFinderService and wizard triggers for automatic GHPC path discovery with Steam-only warning flow
  - Refresh translation update UX with live progress, UTC manifest timestamps, and updated control styling
  - Lower multi-threaded download threshold and expand localization strings for new automation messages
  - Promote build to stable v1.1.1 with revised assembly metadata and resource tweaks

### v1.1.1-beta.1

#### feat: Beta version 1.1.1-beta.1 with BepInEx detection and UI enhancements
  - Add BepInEx detection logic to prevent conflicts with existing installations
  - Introduce BooleanAndToVisibilityConverter for complex UI binding scenarios
  - Update version to 1.1.1-beta.1 with WebView2 dependency integration
  - Enhance string resources and localization infrastructure
  - Improve network service stability and error handling
  - Refine translation manager and update service reliability

### v1.1.0

#### feat: Release version 1.1.0 with polish translation UX and update flows with smarter downloads
  - Add translation language display converter, smart window sizing, and zh-only community shortcuts
  - Guard manual translation management, localize messages, and avoid duplicate startup update checks
  - Rework mod/app update detection to reuse GitHub API URLs with semantic version comparison
  - Enhance IDM-style downloader with work stealing and expand localized logging resources

### v1.1.0-beta.1

#### feat: Beta version 1.1.0-beta.1 with in-app updater and translation upgrades
  - Update Check: Configurable stable/beta update channels with background checks and installer flow
  - Detect manual translation installs, track release timestamps, and surface update availability in UI
  - Revamp download pipeline with IDM-style chunking plus throttled rate-limit warnings
  - Expand UI: update banner, settings update button, log filters/export, enlarged layouts, refreshed strings

### v1.0.1

#### feat: Release version 1.0.1 with enhanced file tracking and translation management
  - Add comprehensive file operation tracking system
  - Implement translation plugin management with enable/disable functionality
  - Enhance network connectivity testing with proxy and direct connection
  - Improve mod installation process with tracked file operations
  - Add translation backup service and unified manifest support
  - Update resource strings with new translation entries
  - Enhance mod uninstall/reinstall capabilities for manual mods
  - Update version to 1.0.1 stable release

### v1.0.0

#### feat: Release version 1.0.0 with improved localization and system enhancements
  - Add mod update checking functionality
  - Enhance resource strings with better organization and new entries
  - Improve logging system with proper localized messages
  - Refactor theme initialization and color handling
  - Update version to 1.0.0 stable release

### v1.0.0-beta.3

#### feat: Add announcement system and improve app stability
- Add announcement service for markdown content display
- Add announcement window UI with proper styling
- Improve application shutdown with resource cleanup
- Fix GitHub workflow prerelease boolean handling
- Enhance main window sizing (1280x720)
- Add value converters for UI binding
- Update mod view models with new properties
- Add comprehensive string resources
- Update version to 1.0.0-beta.3
- Add Markdig package for markdown rendering

### v1.0.0-beta.2-hotfix1

#### hotfix: Improved mod installation to handle both archives and DLL files
- Add proxy server selection enum (GhDmrGg, GhProxyCom, HkGhProxyCom, CdnGhProxyCom, EdgeOneGhProxyCom)
- Enhanced NetworkService with configurable proxy domains
- Improved mod installation to handle both archives and DLL files
- Fixed script-based installation to pass downloaded file path instead of URL
- Added proxy support for git clone operations in TranslationManagerService
- Updated UI to show proxy server selection dropdown in settings
- Reordered setup wizard steps (language selection first)
- Version bump to 1.0.0-beta.2-hotfix1

### v1.0.0-beta.2

#### feat: Add mod backup system and improve mod management features
- Add ModBackupService for automatic mod backup/restore during operations
- Implement dependency and conflict checking for mod installations
- Add GitHub page navigation and game directory access features
- Improve resource management with enhanced string converters
- Add comprehensive localization support for new features
- Update version to 1.0.0-beta.2