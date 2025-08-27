# GHPC Mod Manager Web

[![中文版本](https://img.shields.io/badge/README-%E4%B8%AD%E6%96%87-red)](README.zh-CN.md) | [![English Version](https://img.shields.io/badge/README-English-blue)](README.md)

## Overview

This is the official website repository for **GHPC Mod Manager** - a modern mod management tool designed specifically for Gunner HEAT PC. This repository also serves as the MOD compatibility repository, containing configuration files and documentation for supported mods.

🌐 **Live Website**: [Visit GHPC Mod Manager Website](https://GHPC.DMR.gg/)
🚀 **Main Tool Repository**: [GHPC Mod Manager](https://github.com/RoyZ-iwnl/GHPC-Mod-Manager)

## Supported Mods

Currently supported mods that can be managed through GHPC Mod Manager:

### Active Mods
- **[Pact Increased Lethality](https://github.com/thebeninator/Pact-Increased-Lethality)**
- **[M1A1 Abrams](https://github.com/thebeninator/M1A1Abrams)**
- **[M1A1 Abrams AMP](https://github.com/Cyances/M1A1AbramsAMP)**
- **[M6A2 ADATS](https://github.com/Cyances/M6A2-ADATS)**
- **[NATO ERA](https://github.com/Cyances/NATO-ERA)**
- **[Any Tank Any Campaign](https://github.com/Cyances/Any-Tank-Any-Campaign)**

### More MOD adaptations coming...

## How to Submit a PR for MOD Support

We welcome contributions to expand mod support! Follow these steps to add support for a new mod:

### Step 1: Understand the Configuration Structure

The mod configurations are stored in JSON files located in different directories:
- **Development/Testing**: `/sample_config/` (with comments for guidance)
- **Production**: `/config/` (actual configuration files used by the application)

### Step 2: Configuration Files Overview

#### Main Mod Configuration (`sample_modconfig.jsonc`)
```json
[
  {
    "Id": "YourModId",
    "Name": {
      "en-US": "Your Mod Name in English",
      "zh-CN": "您的模组中文名称"
    },
    "ReleaseUrl": "https://api.github.com/repos/owner/repo/releases/latest",
    "TargetFileNameKeyword": ".zip",
    "MainBinaryFileName": "YourMod.dll",
    "ConfigSectionName": "YourModConfig",
    "InstallMethod": "DirectRelease", // or "Scripted"
    "Requirements": ["BaseModId", "CoreLibraryId"],
    "Conflicts": ["IncompatibleMod1Id", "IncompatibleMod2Id"]
  }
]
```

**Installation Methods:**
- `DirectRelease`: Simple ZIP download and extraction
- `Scripted`: Custom installation using Base64-encoded batch script (see sample for details)

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
      }
    }
  }
}
```

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