# GHPC Mod Manager Web

[![中文版本](https://img.shields.io/badge/README-%E4%B8%AD%E6%96%87-red)](README.zh-CN.md) | [![English Version](https://img.shields.io/badge/README-English-blue)](README.md)

## Overview

This is the official website repository for **GHPC Mod Manager** - a modern mod management tool designed specifically for Gunner HEAT PC. This repository also serves as the MOD compatibility repository, containing configuration files and documentation for supported mods.

🌐 **Live Website**: [Visit GHPC Mod Manager Website](https://GHPC.DMR.gg/)

🚀 **Main Tool Repository**: [GHPC Mod Manager](https://github.com/RoyZ-iwnl/GHPC-Mod-Manager)

## Supported Mods

Currently supported mods that can be managed through GHPC Mod Manager:

### Vehicle Mods
- **[Pact Increased Lethality](https://github.com/RoyZ-iwnl/Pact-Increased-Lethality)** (Priority version)
- **[Pact Increased Lethality](https://github.com/thebeninator/Pact-Increased-Lethality)**
- **[M1A1 Abrams](https://github.com/thebeninator/M1A1Abrams)**
- **[M1A1 Abrams AMP](https://github.com/Cyances/M1A1AbramsAMP)**
- **[Underdogs Enhanced](https://github.com/RoyZ-iwnl/UnderdogsEnhanced)**
- **[Stabilized BMP-1](https://github.com/thebeninator/Stabilized-BMP-1)**
- **[Super M60](https://github.com/RoyZ-iwnl/Super-M60)** (Priority version)
- **[Super M60](https://github.com/Cyances/Super-M60)**
- **[M6A2 ADATS](https://github.com/RoyZ-iwnl/M6A2-ADATS)** (Priority version)
- **[M6A2 ADATS](https://github.com/Cyances/M6A2-ADATS)**
- **[M3A2 Bradley](https://github.com/SovGrenadier/M3A2-Bradley-GHPC)**
- **[50mm Bradley](https://github.com/RoyZ-iwnl/50mm-Bradley)** (Priority version)
- **[50mm Bradley](https://github.com/thebeninator/50mm-Bradley)**
- **[M113 TOW](https://github.com/thebeninator/M113-TOW)**
- **[NATO ERA](https://github.com/Cyances/NATO-ERA)**

### Sound Mods
- **[M2 Bradley Sound Replacement](https://github.com/thebeninator/M2-Bradley-Sound-Replacement)**

### Game Enhancement Mods
- **[M2/BMP2 Fire Rate Toggle](https://github.com/thebeninator/FireRateToggle)**
- **[Bino Aim](https://github.com/thebeninator/BinoAim)**
- **[Weather & Time Control](https://github.com/RoyZ-iwnl/WeatherMod)**
- **[Fast Restock](https://github.com/lucaspevidor/FastRestock)**
- **[LoadoutManager](https://github.com/RoyZ-iwnl/LoadoutManager)**
- **[Random Night Battles](https://github.com/thebeninator/Random-Night-Battles)**
- **[Unrestricted Customizer](https://github.com/thebeninator/CustomizerUnrestricted)**

### Utility Mods
- **[Vehicle Preloader](https://github.com/thebeninator/VehiclePreloader)**
- **[Min HUD](https://github.com/thebeninator/MinHud)**
- **[Any Tank Any Campaign](https://github.com/Cyances/Any-Tank-Any-Campaign)**
- **[GMPC Texture Loader](https://github.com/Andrix44/GMPCTextureLoader)**
- **[Gunner Mod PC](https://github.com/Andrix44/GunnerModPC)**
- **[Cinematic Tools](https://github.com/RoyZ-iwnl/CinematicTools)**

### More MOD adaptations coming...

## How to Submit a PR for MOD Support

We welcome contributions to expand mod support! Follow these steps to add support for a new mod:

### Step 1: Understand the Configuration Structure

The mod configurations are stored in JSON files located in different directories:
- **Development/Testing**: `/sample_config/` (with comments for guidance)
- **Production**: `/config/` (actual configuration files used by the application)

### Step 2: Configuration Files Overview

#### Main Application Configuration (`sample_main.json`)
```json
{
  "ModConfigUrl": "https://GHPC.DMR.gg/config/modconfig.json",
  "ModConfigFallbackUrl": "https://ghpcmm.link/config/modconfig.json",
  "TranslationConfigUrl": "https://github.com/RoyZ-iwnl/ghpc-translation",
  "TranslationConfigFallbackUrl": "",
  "ModI18nUrl": "https://GHPC.DMR.gg/config/mod_i18n.json",
  "ModI18nFallbackUrl": "https://ghpcmm.link/config/mod_i18n.json",
  "ProxyServers": [
    {
      "Id": "GhDmrGg",
      "Domain": "gh.dmr.gg",
      "DisplayName": { "zh-CN": "Cloudflare 1", "en-US": "Cloudflare 1" }
    }
  ]
}
```

**URL Fields:**
- `ModConfigUrl`: Primary URL for mod configuration list
- `ModConfigFallbackUrl`: Fallback URL if primary fails
- `TranslationConfigUrl`: URL for translation configuration repository
- `ModI18nUrl`: Primary URL for mod internationalization strings
- `ModI18nFallbackUrl`: Fallback URL if primary fails

#### Main Mod Configuration (`sample_modconfig.jsonc`)
```jsonc
[
  {
    "Id": "YourModId",
    "Name": {
      "en-US": "Your Mod Name in English",
      "zh-CN": "您的模组中文名称"
    },
    "Description": {
      "en-US": "Description in English",
      "zh-CN": "中文描述"
    },
    "Tags": {
      "modify": { "zh-CN": "载具改装", "en-US": "Vehicle Modify" }
    },
    "SupportedGameVersions": ["20260319"],
    "ReleaseUrl": "https://api.github.com/repos/owner/repo/releases/latest",
    "TargetFileNameKeyword": ".zip",
    "MainBinaryFileName": "YourMod.dll",
    "ConfigSectionName": "YourModConfig",
    "Requirements": ["BaseModId"],
    "Conflicts": ["IncompatibleModId"]
  }
]
```

**Installation Modes:**
- **Default Mode** (no `ReplaceTargetPath`): Files installed to `Mods/` directory
- **Replace Mode** (with `ReplaceTargetPath`): Files placed in target directory with automatic backup

**Replace Mode Example:**
```jsonc
{
  "Id": "SoundMod",
  "ReplaceTargetPath": "GHPC_Data/StreamingAssets",
  "ReplaceFileName": "Weapons.bank",  // Optional: custom filename for single file
  "MainBinaryFileName": ""  // Empty for non-DLL mods
}
```

#### Mod Internationalization (`sample_mod_i18n.json`)
```json
{
  "ModConfigs": {
    "YourModId": {
      "ModId": "YourModId",
      "ConfigLabels": {
        "Config Option Name": {
          "zh-CN": "配置选项中文名",
          "en-US": "Config Option Name"
        }
      },
      "ConfigComments": {
        "Description text": {
          "zh-CN": "描述文字的中文翻译",
          "en-US": "Description text"
        }
      },
      "singlechoice": {
        "Option Name 1,Option Name 2": ["OptionA", "OptionB", "OptionC"]
      },
      "multiplechoice": {
        "MultiSelect Option": ["Choice1", "Choice2", "Choice3"]
      }
    }
  }
}
```

**Field Types:**
- `ConfigLabels`: Translations for configuration option names
- `ConfigComments`: Translations for configuration option descriptions
- `singlechoice`: Options that allow single selection (key can combine multiple related configs with commas)
- `multiplechoice`: Options that allow multiple selection

### Step 3: Create Your Configuration

1. **Fork this repository**
2. **Add your mod configuration to `/sample_config/sample_modconfig.jsonc`**
3. **Add translation strings to `/sample_config/sample_mod_i18n.json`** (if your mod has configurable options)
4. **Test your configuration** by running GHPC Mod Manager locally

### Step 4: Submit Your Pull Request

1. **Create a new branch** with a descriptive name (e.g., `add-support-for-your-mod`)
2. **Commit your changes** with a clear commit message
3. **Submit a pull request** with:
   - Clear description of the mod being added
   - Link to the mod's repository or download page
   - Any special installation requirements or notes

### Configuration Guidelines

- **ModId**: Use a unique, descriptive identifier (no spaces, alphanumeric + underscores)
- **Names**: Provide both English and Chinese translations when possible
- **ReleaseUrl**: Use GitHub API URLs for automatic latest version detection
- **InstallMethod**: Use `DirectRelease` unless custom installation logic is required

## Localization Support

### Translation Files Repository
All translation files for GHPC and its mods are maintained in a separate repository:
**🌍 [GHPC Translation Repository](https://github.com/RoyZ-iwnl/ghpc-translation)**

### How to Contribute Translations

1. **Visit the [GHPC Translation Repository](https://github.com/RoyZ-iwnl/ghpc-translation)**
2. **Follow the XUnity.AutoTranslator format** as described in the [XUnity.AutoTranslator README](https://github.com/bbepis/XUnity.AutoTranslator/blob/master/README.md)
3. **Create your translation files** according to the established format
4. **Submit a Pull Request** to the translation repository

The translation system uses XUnity.AutoTranslator, which provides automatic translation capabilities with support for custom translation files.

## Contributing

We welcome contributions! Please feel free to:
- Report bugs or issues
- Suggest new features
- Add support for new mods
- Improve documentation
- Contribute translations

## License

This project is open source. Please check the main GHPC Mod Manager repository for license details.

## Credits

**Developed by**: DrakeX_ (AKA RoyZ)  
**Links**: [Bilibili](https://space.bilibili.com/3493285595187364) | [GitHub](https://github.com/RoyZ-iwnl/GHPC-Mod-Manager)