# GHPC Mod Manager Web

[![中文版本](https://img.shields.io/badge/README-%E4%B8%AD%E6%96%87-red)](README.zh-CN.md) | [![English Version](https://img.shields.io/badge/README-English-blue)](README.md)

## 项目概述

这是 **GHPC Mod Manager** 的官方网站仓库 - 一个专为 Gunner HEAT PC 设计的现代化模组管理工具。此仓库也作为 MOD 兼容性仓库，包含支持模组的配置文件和文档。

🌐 **在线网站**: [访问 GHPC Mod Manager 网站](https://GHPC.DMR.gg/)

🚀 **主工具仓库**: [GHPC Mod Manager](https://github.com/RoyZ-iwnl/GHPC-Mod-Manager)

## 支持的模组

目前通过 GHPC Mod Manager 支持管理的模组：

### 载具模组
- **[华约增强模组 (Pact Increased Lethality)](https://github.com/RoyZ-iwnl/Pact-Increased-Lethality)** (优先更新版)
- **[华约增强模组 (Pact Increased Lethality)](https://github.com/thebeninator/Pact-Increased-Lethality)**
- **[M1A1艾布拉姆斯 (M1A1 Abrams)](https://github.com/thebeninator/M1A1Abrams)**
- **[M1A1 Abrams AMP (M1A1艾布拉姆斯AMP)](https://github.com/Cyances/M1A1AbramsAMP)**
- **[弱势载具增强 (Underdogs Enhanced)](https://github.com/RoyZ-iwnl/UnderdogsEnhanced)**
- **[BMP-1 稳定器 (Stabilized BMP-1)](https://github.com/thebeninator/Stabilized-BMP-1)**
- **[超级M60 (Super M60)](https://github.com/RoyZ-iwnl/Super-M60)** (优先更新版)
- **[超级M60 (Super M60)](https://github.com/Cyances/Super-M60)**
- **[M6A2 ADATS (M6A2"阿达茨"布雷德利)](https://github.com/RoyZ-iwnl/M6A2-ADATS)** (优先更新版)
- **[M6A2 ADATS (M6A2"阿达茨"布雷德利)](https://github.com/Cyances/M6A2-ADATS)**
- **[M3A2 Bradley (M3A2 超级布雷德利)](https://github.com/SovGrenadier/M3A2-Bradley-GHPC)**
- **[50毫米布雷德利 (50mm Bradley)](https://github.com/RoyZ-iwnl/50mm-Bradley)** (优先更新版)
- **[50毫米布雷德利 (50mm Bradley)](https://github.com/thebeninator/50mm-Bradley)**
- **[M113 TOW (M113 "陶")](https://github.com/thebeninator/M113-TOW)**
- **[NATO ERA (北约爆反)](https://github.com/Cyances/NATO-ERA)**

### 音效模组
- **[M2 Bradley Sound Replacement (M2布雷德利声音替换)](https://github.com/thebeninator/M2-Bradley-Sound-Replacement)**

### 游戏增强模组
- **[B键M2/BMP2射速切换 (M2/BMP2 Fire Rate Toggle)](https://github.com/thebeninator/FireRateToggle)**
- **[车长超控瞄准放大限制解除 (Bino Aim)](https://github.com/thebeninator/BinoAim)**
- **[天气与时间控制 (Weather & Time Control)](https://github.com/RoyZ-iwnl/WeatherMod)**
- **[快速搬弹 (Fast Restock)](https://github.com/lucaspevidor/FastRestock)**
- **[弹药架管理器 (LoadoutManager)](https://github.com/RoyZ-iwnl/LoadoutManager)**
- **[随机夜战 (Random Night Battles)](https://github.com/thebeninator/Random-Night-Battles)**
- **[无限制自定义 (Unrestricted Customizer)](https://github.com/thebeninator/CustomizerUnrestricted)**

### 实用工具模组
- **[载具预载支持模块 (Vehicle Preloader)](https://github.com/thebeninator/VehiclePreloader)**
- **[最小化UI (Min HUD)](https://github.com/thebeninator/MinHud)**
- **[自定义战役坦克 (Any Tank Any Campaign)](https://github.com/Cyances/Any-Tank-Any-Campaign)**
- **[贴图更换工具 (GMPC Texture Loader)](https://github.com/Andrix44/GMPCTextureLoader)**
- **[GMPC增强插件 (Gunner Mod PC)](https://github.com/Andrix44/GunnerModPC)**
- **[电影工具 (Cinematic Tools)](https://github.com/RoyZ-iwnl/CinematicTools)**

### 更多MOD适配中...

## 如何提交 PR 增加模组支持

我们欢迎贡献来扩展模组支持！按照以下步骤添加新模组支持：

### 步骤 1: 了解配置结构

模组配置存储在不同目录的 JSON 文件中：
- **开发/测试用**: `/sample_config/` (带注释的示例文件)
- **生产环境**: `/config/` (应用程序实际使用的配置文件)

### 步骤 2: 配置文件概述

#### 主应用配置 (`sample_main.json`)
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

**URL 字段说明：**
- `ModConfigUrl`: 模组配置列表的主 URL
- `ModConfigFallbackUrl`: 主 URL 失败时的备用 URL
- `TranslationConfigUrl`: 翻译配置仓库的 URL
- `ModI18nUrl`: 模组国际化字符串的主 URL
- `ModI18nFallbackUrl`: 主 URL 失败时的备用 URL

#### 主模组配置 (`sample_modconfig.jsonc`)
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

**安装模式：**
- **默认模式**（无 `ReplaceTargetPath`）：文件安装到 `Mods/` 目录
- **替换模式**（有 `ReplaceTargetPath`）：文件放置到目标目录，自动备份原文件

**替换模式示例：**
```jsonc
{
  "Id": "SoundMod",
  "ReplaceTargetPath": "GHPC_Data/StreamingAssets",
  "ReplaceFileName": "Weapons.bank",  // 可选：单文件下载时指定目标文件名
  "MainBinaryFileName": ""  // 非DLL模组留空
}
```

#### 模组本地化支持 (`sample_mod_i18n.json`)
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

**字段类型说明：**
- `ConfigLabels`: 配置选项名称的翻译
- `ConfigComments`: 配置选项描述的翻译
- `singlechoice`: 单选选项（键名可用逗号组合多个相关配置）
- `multiplechoice`: 多选选项

### 步骤 3: 创建您的配置

1. **Fork 此仓库**
2. **将您的模组配置添加到 `/sample_config/sample_modconfig.jsonc`**
3. **将翻译字符串添加到 `/sample_config/sample_mod_i18n.json`**（如果您的模组有可配置选项）
4. **通过本地运行 GHPC Mod Manager 来测试您的配置**

### 步骤 4: 提交拉取请求

1. **创建新分支**，使用描述性名称（如 `add-support-for-your-mod`）
2. **提交您的更改**，使用清晰的提交信息
3. **提交拉取请求**，包含：
   - 被添加模组的清楚描述
   - 模组仓库或下载页面的链接
   - 任何特殊的安装要求或注意事项

### 配置指南

- **ModId**: 使用唯一的、描述性的标识符（无空格，字母数字 + 下划线）
- **Names**: 尽可能提供英文和中文翻译
- **ReleaseUrl**: 使用 GitHub API URL 进行自动最新版本检测
- **InstallMethod**: 除非需要自定义安装逻辑，否则使用 `DirectRelease`

## 本地化支持

### 翻译文件仓库
GHPC 及其模组的所有翻译文件都在单独的仓库中维护：
**🌍 [GHPC 翻译仓库](https://github.com/RoyZ-iwnl/ghpc-translation)**

### 如何贡献翻译

1. **访问 [GHPC 翻译仓库](https://github.com/RoyZ-iwnl/ghpc-translation)**
2. **遵循 XUnity.AutoTranslator 格式**，参考 [XUnity.AutoTranslator README](https://github.com/bbepis/XUnity.AutoTranslator/blob/master/README.md)
3. **按照既定格式创建您的翻译文件**
4. **向翻译仓库提交拉取请求**

翻译系统使用 XUnity.AutoTranslator，它提供自动翻译功能并支持自定义翻译文件。

## 贡献

我们欢迎贡献！请随时：
- 报告错误或问题
- 建议新功能
- 添加新模组支持
- 改进文档
- 贡献翻译

## 许可证

此项目是开源的。请查看主 GHPC Mod Manager 仓库获取许可证详情。

## 制作人员

**开发者**: DrakeX_ (AKA RoyZ)  
**链接**: [Bilibili](https://space.bilibili.com/3493285595187364) | [GitHub](https://github.com/RoyZ-iwnl/GHPC-Mod-Manager)