# GHPC Mod Manager Web

[![中文版本](https://img.shields.io/badge/README-%E4%B8%AD%E6%96%87-red)](README.zh-CN.md) | [![English Version](https://img.shields.io/badge/README-English-blue)](README.md)

## 项目概述

这是 **GHPC Mod Manager** 的官方网站仓库 - 一个专为 Gunner HEAT PC 设计的现代化模组管理工具。此仓库也作为 MOD 兼容性仓库，包含支持模组的配置文件和文档。

🌐 **在线网站**: [访问 GHPC Mod Manager 网站](https://GHPC.DMR.gg/)
🚀 **主工具仓库**: [GHPC Mod Manager](https://github.com/RoyZ-iwnl/GHPC-Mod-Manager)

## 支持的模组

目前通过 GHPC Mod Manager 支持管理的模组：

### 活跃模组
- **[华约增强模组 (Pact Increased Lethality)](https://github.com/thebeninator/Pact-Increased-Lethality)** - 增强华约阵营装备性能，提升战斗体验
- **[M1A1艾布拉姆斯 (M1A1 Abrams)](https://github.com/thebeninator/M1A1Abrams)** - M1A1主战坦克模组，增加新载具和装备

### 更多MOD适配中...

## 如何提交 PR 增加模组支持

我们欢迎贡献来扩展模组支持！按照以下步骤添加新模组支持：

### 步骤 1: 了解配置结构

模组配置存储在不同目录的 JSON 文件中：
- **开发/测试用**: `/sample_config/` (带注释的示例文件)
- **生产环境**: `/config/` (应用程序实际使用的配置文件)

### 步骤 2: 配置文件概述

#### 主模组配置 (`sample_modconfig.jsonc`)
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
    "InstallMethod": "DirectRelease" // 或 "Scripted"
  }
]
```

**安装方式：**
- `DirectRelease`: 简单的 ZIP 下载和解压
- `Scripted`: 使用 Base64 编码的批处理脚本进行自定义安装（详见示例）

#### 模组国际化 (`sample_mod_i18n.json`)
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