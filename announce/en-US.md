# Welcome to GHPC Mod Manager

## Announcement

### 2026-05-01
- v1.3.4 stable release is now available with skip check options, translation install optimization, hardware info collection. See the [changelog](#v134) below for details.

### 2026-04-14
- v1.3.3 stable release is now available with new mods banner in installed page, navigation service refactor, and translation backup extension migration. See the [changelog](#v133) below for details.

### 2026-04-05
- v1.3.2 stable release is now available with multi-format archive support, new mods detection banner, and manager version requirement check. See the [changelog](#v132) below for details.

### 2026-03-30
- v1.3.1 stable release is now available with fixing some bugs in v1.3.0, previous installation detection, backup cleanup refactor, and scripted mode removal. See the [changelog](#v131) below for details.
- v1.3.0 stable release is now available with game version detection refactor, UI overhaul, Replace install mode, integrity checking, custom title bar, MessageDialog system, and Mod Info Dumper. See the [changelog](#v130) below for details.

### 2026-03-16
- v1.2.3 stable release is now available with GitHub API token encryption, announcement tracking, startup mod update check, and network detection refactor. See the [changelog](#v123) below for details.

### 2026-03-12
- v1.2.2 stable release is now available with MOD configuration enhancements and setup wizard improvements. See the [changelog](#v122) below for details.

### 2026-03-05
- v1.2.1 stable release is now. See the [changelog](#v121) below for details.

### 2026-02-28
- v1.2.0 stable release is now available with modular UI navigation, remote config service, and enhanced MelonLoader management. See the [changelog](#v120) below for details.

### 2026-02-19

- v1.1.4 stable release is now available with MelonLoader management and stability fixes. See the [changelog](#v114) below for details.
- v1.1.3-beta.1 beta version is now available with GitHub API token support and parallel loading optimization. See the [changelog](#v113-beta1) below for details.
- Configure GitHub Token to bypass rate limits (60→5000 requests/hour).
- Optimized MOD loading and update checking with parallel processing to significantly reduce startup time.

### 2026-02-18
- Some mods are outdated for the latest Steam version, so we’ve released priority version updates. Please uninstall the originals mods before use, your settings will be saved.Contact me for more priority mod updates.
  - Pact Increased Lethality
  - M6A2 ADATS
  - 50mm Bradley
- When you toggle off the priority version mod may cause a display bug on v1.1.2, It shows both versions installed, but only the priority one is real. Don't touch the original mod—just toggle the priority version. I'll release a beta to fix the display bug soon. Remember to uninstall the original before installing the priority version.

### 2026-01-20

- v1.1.2 stable release is now available with singleton navigation optimization and resource regeneration. See the [changelog](#v112) below for details.

### 2025-12-11

- v1.1.2-beta.1 beta version is now available with offline mode, launch validation, and MOD update date display. See the [changelog](#v112-beta1) below for details.
- If you are using PACT IL or M1A1 mods or M113 TOW,please install "Vehicle Preloader" Mod for the latest GHPC update(20251030.2)

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

### v1.3.4
#### feat: Release version 1.3.4 with skip check options, translation install optimization, hardware info collection
- Bump version to 1.3.4
- Add System.Management package for hardware information collection
- Add SkipConflictCheck and SkipIntegrityCheck settings to skip checks on game launch
- Add skip check options UI in SettingsView
- Implement conditional conflict and integrity checks based on skip settings in MainViewModel
- Removed herobrine
- Refactor translation installation to two-phase commit (download first, then extract) to prevent partial installations on failure
- Add DownloadXUnityArchiveAsync and DownloadTranslationArchiveAsync methods for in-memory download
- Fix disabled mod file detection to only include root-level DLL files, skip subdirectory resource files
- Add hardware information collection in ModInfoDumper (CPU, Memory, GPU) using System.Management
- Add Icons.xaml resource dictionary with dialog, title bar, and general UI icons
- Add Icons.xaml to App.xaml merged dictionaries
- Update localization strings for new features

### v1.3.3
#### feat: Release version 1.3.3 with new mods banner in installed page, navigation service refactor, and translation backup extension migration
- Bump version to 1.3.3
- Add new mods banner display in InstalledModsView with navigation to Mod Browser
- Add PageNavigationRequested event and NavigateToPage/NavigateToModBrowser/NavigateToInstalledMods/NavigateToTranslation methods in NavigationService
- Add GoToModBrowser localization string for banner button
- Add ShowUninstalledOnly field in AppSettings for persisting mod browser filter state
- Sync new mods banner data from ModBrowserViewModel to InstalledModsViewModel
- Refactor GoToInstalledMods and GoToTranslationManagement to use NavigationService
- Migrate translation plugin backup extension from .dllbak to .GHPCMMBAK with automatic migration on load
- Add backward compatibility for old .dllbak backup extension detection
- Fix download progress percentage cap at 100% to prevent overflow from inaccurate Content-Length
- Fix config comment parsing to treat all lines starting with # as comments
- Remove ITranslationBackupService dependency from App.xaml.cs and MainViewModel
- Update new mods preview list to show all detected mod names instead of limiting to 3

### v1.3.2
#### feat: Release version 1.3.2 with multi-format archive support, new mods detection banner, and manager version requirement check
- Bump version to 1.3.2
- Add SharpCompress package for multi-format archive extraction (RAR, 7z, TAR, GZ, BZ2, XZ)
- Add ExtractArchiveAsync method in TrackedFileOperations for unified archive handling
- Refactor Replace mode installation to use SharpCompress for archive extraction
- Add IModCatalogStateService for persisting mod catalog state snapshots
- Add new mods detection and banner display in ModBrowserView
- Add RequiredManagerVersion field in ModConfig for minimum manager version requirement
- Add MeetsRequiredVersion method in UpdateService for version requirement checking
- Add manager version requirement check before mod install/update/reinstall
- Add GoToSettingsCancel dialog button type for version requirement prompt
- Display short git hash in window title bar (e.g., v1.3.2 (abc1234))
- Cleanup unused localization strings and unify string keys
- Adjust overlay layer ordering in MainView.xaml

### v1.3.1
#### feat: Release version 1.3.1 with previous installation detection, backup cleanup refactor, and scripted mode removal
- Bump version to 1.3.1
- Add PreviousInstallationService to detect and track previous installation via registry
- Add previous installation detection dialog on first run with "Open Folder" and "Ignore" options
- Add MessageDialogButton.OpenFolderIgnore and corresponding result types
- Add CommandLineArgs static class replacing DevMode for centralized argument parsing
- Remove deprecated Scripted install mode and all related code (InstallScript_Base64, UninstallScript_Base64, EnableScript_Base64)
- Delete DevMode.cs with functionality migrated to CommandLineArgs.cs
- Remove unused chunk download and persistent cache methods from NetworkService
- Remove unused ConfigurationItem class from MainViewModel
- Remove duplicate logging calls in TranslationManagerService
- Fix LoggingService date parsing to use filename instead of unreliable File.GetCreationTime
- Fix ModBackupService to use Copy+Delete instead of Move for file overwrite handling
- Add manifest migration backup/restore mechanism in ModManagerService.Replace.cs
- Add CleanupOrphanedDisabledDirectoriesAsync to clean orphaned backup directories without manifest records
- Preserve manual mod backups when manifest is missing to avoid accidental deletion
- Add ProcessService IDisposable implementation for proper timer cleanup
- Adjust MainView layout and status pill positioning
- Adjust SettingsView field spacing and section margins
- Simplify TranslationView by removing top toolbar, move update button into card
- Add localization strings for previous installation detection and backup cleanup
- Remove deprecated Scripted mode localization strings
- Update integrity check hint text to suggest "reinstall" instead of just "fix or reinstall"

### v1.3.0
#### feat: Release version 1.3.0 with game version detection refactor, UI overhaul, Replace install mode, integrity checking, custom title bar, MessageDialog system, and Mod Info Dumper
- Bump version to 1.3.0 (via 1.2.4-beta.1 and 1.3.0-beta.1)
- Refactor game version detection: initially from sharedassets0.assets (no MelonLoader dependency), then migrated to globalgamemanagers
- Add fallback to MelonLoader Latest.log for game version detection when assets method fails
- Add regex pattern matching for date-format version strings, updated to match full format like 0.1.0-alpha+20260319.1
- Add expected size and digest verification for update downloads
- Refactor theme system with Foundation design tokens (typography, spacing, radius, shadow)
- Add PageStyles.xaml for page-level styles and refactor ControlStyles.xaml
- Refactor all view XAMLs with improved layout and styling
- Add custom window title bar with WindowChrome and WindowTitleBar control (minimize/maximize/close buttons)
- Implement WM_GETMINMAXINFO hook for proper maximized window sizing
- Add Replace install method and ModManagerService.Replace.cs for direct game file replacement
- Add InstalledFileInfo structured file information with SHA256 and file size
- Upgrade install manifest SchemaVersion to v2 with backward compatibility
- Add managed mod integrity checking with missing/modified file detection
- Add delisted mod support - hide from list but warn on launch if installed
- Add status banners for delisted mods and unknown fields warnings
- Add unknown config fields detection for forward compatibility
- Add game version compatibility check before mod install/update
- Enhance Dev mode to support custom main config URL via -dev:"path" or -dev="path"
- Improve announcement window with rich text and interactive elements
- Add MessageDialog system replacing MessageBox for consistent styling, with MessageDialogHelper static class (Show/Confirm/ShowWarning etc), IDialogService/DialogService for DI, and MessageDialog enums for button/icon types
- Replace all MessageBox.Show calls with MessageDialogHelper across services and VMs
- Add ModInfoDumper tool with CopyModInfo command (copy mod list + SHA256 to clipboard) and PackAllInfo command (create diagnostic ZIP with logs and configs)
- Add localization strings for game version detection, integrity check, delisted mods, script execution, ModInfoDumper, and MessageDialog features

### v1.2.3
#### feat: Release version 1.2.3 with announcement tracking, startup mod update check, and network detection refactor
- Bump version to 1.2.3 (stable release from beta.2)
- Add SecureStorageService using Windows DPAPI for sensitive data encryption
- Implement GitHub API token encryption with automatic migration from plaintext
- Add UnprotectWithMigrationDetection method to detect and migrate legacy plaintext tokens
- Add announcement MD5 tracking to identify new announcements and skip already-seen content
- Add "Do not show before update" checkbox in announcement dialog for user preference
- Add "Show Announcement" button in settings page for manual access
- Add startup mod update check for users with GitHub API token or proxy enabled
- Optimize first-run experience by skipping main config load and version cleanup to avoid triggering GitHub API
- Split network connectivity check into CheckNetworkConnectionAsync (main.json fallback chain) and CheckGitHubConnectionAsync (GitHub API test)
- Improve main config connectivity test to iterate through all fallback candidates
- Add TestConnectionAsync helper method for GitHub connectivity test with proxy support
- Update SetupWizardViewModel to use CheckGitHubConnectionAsync for wizard network check
- Refactor SetupWizard network detection into three-phase flow: main config connectivity test, proxy list update, GitHub connectivity test
- Enforce network detection completion before proceeding from Step 2 in setup wizard
- Add MainConfigTestResult model and TestMainConfigConnectivityAsync method for connectivity testing
- Refactor ModViewModel properties with INotifyPropertyChanged for UI auto-refresh
- Fix CanUpdate logic to normalize version strings (strip 'v' prefix) for comparison
- Add ReinstallMod command for quick mod reinstallation
- Add GitHub API token permission hint (public_repo only required)
- Improve translation resource update check with force refresh for token/proxy users
- Add localization strings for network detection, announcement, and mod update check

### v1.2.2
#### feat: Release version 1.2.2 with MOD configuration enhancements and setup wizard improvements
- Bump version to 1.2.2 (stable release from 1.2.1)
- Add multiple-choice configuration support for MOD settings with TOML array format output
- Add single-choice configuration support with localized option labels
- Add MOD configuration reset feature to clear config section from MelonPreferences.cfg
- Add "Redownload & Reinstall" button for MODs with existing backup to force fresh download
- Add file download verification with expected size and digest parameters
- Add manual MOD uninstall button in MOD detail view
- Improve backup state sync to show backup status for latest version only
- Show GitHub proxy settings only for zh-CN users in setup wizard
- Show network help button only for zh-CN users
- Simplify setup wizard flow - all users go through network check step
- Add MelonLoader version list load failure warning with retry hint
- Add ChineseLanguageToVisibilityConverter for language-specific UI elements
- Add localization strings for configuration reset and MelonLoader load warning

### v1.2.1
#### feat: Release version 1.2.1 with DNS over HTTPS support for Chinese users
- Bump version to 1.2.1 (stable release from beta.1)
- Add DNS over HTTPS (DoH) connector service with multi-endpoint fallback support
- Implement DnsOverHttpsConnector with 6 preset DoH endpoints (223.5.5.5, 1.12.12.12, 223.6.6.6, 120.53.53.53, doh.apad.pro, v.recipes)
- Add DNS query cache with TTL-based expiration (30s-10min)
- Auto fallback to system DNS when DoH fails
- Refactor HttpClient configuration to use ConfigureHttpClientDefaults
- Replace HttpClientHandler with SocketsHttpHandler for better performance
- Integrate DoH via ConnectCallback for transparent DNS resolution
- Add session-based memory cache for non-GitHub resources
- ModConfig and ModI18nConfig now use session cache to avoid duplicate requests
- Add ClearSessionCache method and clear on manual refresh
- Add DoH toggle in settings (visible only for zh-CN users)
- Fix game running state not synced on startup
- Add localization string SessionCacheCleared

### v1.2.0
#### feat: Release version 1.2.0 with modular UI navigation and enhanced MelonLoader management
- Split MainView into dedicated ModBrowserView, InstalledModsView, ModDetailView, and TranslationView for cleaner navigation
- Add MainConfigService with remote fetch, 1-hour cache, and built-in fallback URLs for centralized config management
- Introduce ModBrowserViewModel with tag-based chip filtering, search, and install/update actions
- Add ModDetailViewModel for per-mod detail page with dependency/conflict display and changelog
- Add InstalledModsViewModel for managing installed mods with enable/disable/uninstall operations
- Remove UnifiedManifest model in favor of MainConfig-driven remote configuration
- Add DevMode model for developer-mode local config override
- Add MelonLoader file manifest to track installed files during installation, enabling precise uninstall without touching user data directories
- Add VersionCleanupService to auto-remove obsolete files from previous versions on startup by comparing release ZIPs
- Improve MelonLoader version detection to read from MelonLoader.dll FileVersion first, falling back to Latest.log
- Add GetCurrentGameVersionAsync to read game version from Latest.log for compatibility display in MOD browser
- Replace MelonLoader-not-installed popup with non-blocking overlay with direct install navigation button
- Refactor game-running overlay to cover content area only, keeping stop button accessible in status bar
- Display supported game versions as colored badges in MOD browser — green for match, amber for mismatch
- Refactor proxy server selection to SelectedProxyServer object binding in Settings and Setup Wizard
- Auto-refresh proxy server list from remote config when entering Step 2 of Setup Wizard
- Show dependency dialog with MOD display names instead of raw mod IDs
- Reset version cleanup flag before self-update to trigger cleanup after next launch
- Add "Open Game Folder" button to main view for quick file explorer access
- Fix setup wizard skipping unnecessary version cleanup on first install by pre-setting CleanupDoneForVersion
- Inject IUpdateService into SetupWizardViewModel to support version-aware setup completion
- Expand localization strings for new views and navigation labels
- Publish as single-file executable targeting win-x64
- Bump version to 1.2.0 stable release and update assembly metadata

### v1.1.4

#### feat: Release version 1.1.4 with MelonLoader management and stability fixes
  - Add MelonLoader management panel in Settings: view installed version, enable/disable, and reinstall from GitHub releases
  - Add MelonLoader disabled overlay on main view to indicate mod operations are blocked
  - Detect installed MelonLoader version by parsing MelonLoader/Latest.log
  - Add GitHub API Token field to Setup Wizard network configuration page
  - Enforce proxy/token mutual exclusion in Setup Wizard: enabling proxy clears token and vice versa
  - Fix game-running check to occur after download completes, preventing file write conflicts
  - Fix MOD file matching to use exact filename comparison instead of partial match
  - Fix backup restore to support backup_paths.json path mapping and detect empty backups
  - Fix backup directory cleanup to recursively delete residual files including backup_paths.json
  - Fix MOD sort order to preserve original JSON order for non-installed mods instead of alphabetical
  - Fix manifest save during load to use await instead of fire-and-forget
  - Bump version to 1.1.4 with updated assembly metadata

### v1.1.3-beta.1

#### feat: Beta version 1.1.3-beta.1 with GitHub API token support and parallel loading optimization
  - Add GitHub API token authentication to bypass rate limits (60→5000 requests/hour) with automatic direct connection
  - Optimize MOD loading with parallel GitHub version fetching to reduce startup time
  - Parallelize version update checks across all MODs for faster refresh
  - Fix backup file name matching logic by extracting original filename from backup path
  - Fix IsSupportedManualMod flag for manually installed MODs
  - Add translation tips panel warning about FPS impact and hotkey conflicts
  - Disable proxy settings when GitHub token is configured to ensure direct API access
  - Bump version to 1.1.3-beta.1 with updated assembly metadata

### v1.1.2

#### feat: Release version 1.1.2 with singleton navigation optimization and resource regeneration
  - Convert MainViewModel and MainView to singleton lifetime to prevent recreation during navigation
  - Include 1.1.2-beta.1 update

### v1.1.2-beta.1

#### feat: Beta version 1.1.2-beta.1 with offline mode, launch checks, and MOD update date display
  - Introduce offline mode with graceful fallback when network unavailable, allowing local operations while blocking installs/updates
  - Add pre-launch conflict and dependency validation with user confirmation dialogs to prevent runtime issues
  - Display MOD update dates with relative time format (today/yesterday/X days ago) alongside version numbers
  - Preserve disabled MOD backups during cleanup, only remove uninstalled backups to maintain rollback capability
  - Enhance GitHub rate limit message with proxy server switching suggestion
  - Simplify .gitignore by removing AI assistant file exclusions
  - Bump version to 1.1.2-beta.1 with updated assembly metadata

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