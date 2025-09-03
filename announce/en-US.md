# Welcome to GHPC Mod Manager

## Announcement

### 2025-09-03

- GHPC version 20250902 has been released. Some mods may not be compatible. Please install or update accordingly.

## Changelog

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