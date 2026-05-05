# 欢迎使用GHPC 模组管理器

## 公告

### 2026-05-05
- v1.3.5 正式版已发布，新增单实例检测、协议激活(ghpcmm://)、平滑页面过渡、UI改进与旧版本迁移支持，详情见下方[更新日志](#v135)。

### 2026-05-01
- v1.3.4 正式版已发布，新增跳过检查选项、翻译安装优化、硬件信息收集，详情见下方[更新日志](#v134)。

### 2026-04-14
- v1.3.3 正式版已发布，新增已安装页新上架Mod横幅、导航服务重构与翻译备份后缀迁移，详情见下方[更新日志](#v133)。

### 2026-04-05
- v1.3.2 正式版已发布，新增多格式压缩包支持、新上架Mod横幅与管理器版本要求检查，详情见下方[更新日志](#v132)。

### 2026-03-30
- v1.3.1 正式版已发布，修复了v1.3.0存在的部分问题，新增旧安装检测、备份清理重构与移除Scripted模式，详情见下方[更新日志](#v131)。
- v1.3.0 正式版已发布，包含游戏版本检测重构、UI全面重构、Replace安装模式、完整性检查、自定义标题栏、MessageDialog系统与Mod信息导出工具，详情见下方[更新日志](#v130)。

### 2026-03-16
- v1.2.3 正式版已发布，新增GitHub API Token加密存储、公告追踪、启动Mod更新检查与网络检测重构，详情见下方[更新日志](#v123)。

### 2026-03-12
- v1.2.2 正式版已发布，新增MOD配置增强与安装向导优化，详情见下方[更新日志](#v122)。
- ⚠️注意华约增强优先更新版已经可以弃之不用，官方最新版已经支持了新版本游戏，您的配置不会丢失。

### 2026-03-05
- v1.2.1 正式版已发布，新增DNS over HTTPS支持，改善国内用户访问体验，详情见下方[更新日志](#v121)。

### 2026-02-28
- v1.2.0 正式版已发布，重构了模块化UI导航，新增远程主配置服务与MelonLoader文件追踪机制，详情见下方[更新日志](#v120)。

### 2026-02-19

- v1.1.4 正式版已发布，新增MelonLoader管理功能与多项稳定性修复，详情见下方[更新日志](#v114)。
- v1.1.3-beta.1 测试版已发布，新增GitHub API Token支持与并行加载优化，详情见下方[更新日志](#v113-beta1)。
- 配置GitHub Token后可突破API频率限制（60→5000请求/小时）需代理或Steamcommunity302或Steam++等反代。
- 优化MOD加载与更新检查流程，采用并行处理大幅缩短启动时间。

### 2026-02-18
- 由于部分mod作者维护不及时，导致无法适配Steam最新版，我们为以下mod推出优先更新版，方便大家使用，使用前请先卸载原版，您的设置不会丢失。
  - 华约增强模组
  - M6A2 "阿达茨"布雷德利
  - 50毫米布雷德利
- 当您切换优先更新版mod时，可能出现显示异常：界面会同时显示两个已安装版本，但实际优先更新版有效。请勿操作原始mod——仅需切换优先更新版开关即可。我将尽快发布修复显示异常的测试版。安装优先版本前，请务必先卸载原始版本。

### 2026-01-20

- v1.1.2 正式版已发布，优化导航单例模式与资源重新生成，详情见下方[更新日志](#v112)。
- 启用代理加速的用户请使用gh.dmr.gg(Cloudflare 1)获得更新后的访问体验

### 2025-12-11

- v1.1.2-beta.1 测试版已发布，新增离线模式、启动检查与MOD更新日期显示，详情见下方[更新日志](#v112-beta1)。
- 如果你在使用 华约增强 或 M1A1模组 或 M113 TOW请安装"载具预载支持模块"以兼容最新的GHPC更新（20251030.2）

### 2025-10-11

- v1.1.1 正式版已发布，新增Steam自动搜寻与翻译体验升级，详情见下方[更新日志](#v111)。

### 2025-10-09

- v1.1.1-beta.1 测试版已发布，新增BepInEx检测逻辑与界面增强功能，详情见下方[更新日志](#v111-beta1)。
- 中文翻译文件已经更新适配游戏版本20250930.1

### 2025-10-05

- v1.1.0版本正式版已发布，优化翻译体验与更新流程并强化多线程下载，beta版本用户可直接使用内置更新下载更新，详情见下方[更新日志](#v110)。
- 新增Customizer Unrestricted (无限制自定义)Mod支持

### 2025-10-01

- v1.1.0-beta.1 测试版已发布，新增应用内更新与翻译升级，详情见下方[更新日志](#v110-beta1)。
- 新增BMP-1稳定器Mod支持

### 2025-09-23

- v1.0.1 已发布！修正了若干小问题，具体见下方[更新日志](#v101)。

### 2025-09-04

- v1.0.0已发布！期待反馈和意见！如遇MOD间冲突也可以报告，以便添加冲突检测。
- 已知翻译系统的安装可能会有一些问题，如遇翻译系统安装卡住，请尝试等待几分钟。

### 2025-09-03

- GHPC版本20250902已发布，部分mod可能出现不适配的情况，请根据实际情况安装或更新。

## 更新日志

### v1.3.5
#### feat: 发布1.3.5版本，新增单实例检测、协议激活、UI改进与旧版本迁移
- 版本升级至1.3.5
- 更新版权年份至2026
- 新增基于互斥锁的单实例检测，防止多实例同时运行
- 新增基于命名管道的实例间IPC通信，支持协议激活
- 新增协议激活支持（ghpcmm://），支持深度链接与主题解锁
- 新增IProtocolActivationService、IProtocolIpcServer、NamedPipeProtocolIpcServer和ProtocolIpcClient用于协议处理
- 新增PageTransitionBehavior和TransitionContentControl实现平滑页面过渡动画
- 新增ModDetailViewModel和SettingsViewModel中的游戏运行状态检测
- 新增SettingsView中的启动时打开网站设置选项
- 新增主题变更事件订阅，实现实时主题同步
- 改进ModDetailView界面，使用开关切换替代按钮进行Mod启用/禁用
- 新增RelatedModInfo的IsDelisted字段，在依赖/冲突显示中跳过已下架Mod
- 改进旧版本检测，新增版本检查与启动选项（适用于1.3.5及以上版本）
- 新增MessageDialog中的LaunchApp按钮类型，用于启动旧版本
- 新增SetupWizardViewModel中的IsVersionAtLeast方法用于版本比较
- 将关于部分移至SettingsView顶部，提升可见性
- 新增ModInfoDumper中的注册表信息收集功能
- 新增ThemeTracker辅助类，跟踪当前主题状态
- 优化主题切换，跳过冗余的主题应用操作
- 重构主题资源字典插入逻辑，改为追加到末尾以确保样式正确覆盖
- 重构ModBrowserView卡片布局，从3行改为紧凑3行设计
- 将状态徽章移至ModBrowserView卡片右上角
- 优化浏览器卡片描述文字显示，支持换行和裁剪
- 更新OutlinedButtonStyle改用透明背景和OnSurface边框
- 调整OutlinedButton悬停和禁用状态样式
- 新增ListBox控件默认ItemTemplate，包含项目符号
- 移除重复的CompactFilledButtonStyle和CompactOutlinedButtonStyle定义
- 将InstalledModsView中Mod标题颜色从Accent改为OnSurface
- 隐藏InstalledModsView中的LocalizedTags显示
- 修复ResponsiveCardWidthConverter绑定从ActualWidth改为ViewportWidth
- 统一徽章圆角使用DynamicResource BadgeCornerRadius
- 新增国际化字符串支持新功能（CannotChangeGamePathWhileRunning、PreviousInstallationLaunchApp、OpenWebsiteOnStartup、SupportAuthor等）
- 新增mciSendString Windows API支持音频重叠播放
- 移除了HEROBRINE

### v1.3.4
#### feat: 发布1.3.4版本，新增跳过检查选项、翻译安装优化、硬件信息收集
- 版本升级至1.3.4
- 新增System.Management包用于硬件信息收集
- 新增SkipConflictCheck和SkipIntegrityCheck设置，支持启动游戏时跳过冲突和完整性检查
- 新增设置页跳过检查选项UI
- 在MainViewModel中根据跳过设置实现条件性冲突和完整性检查
- 移除herobrine
- 重构翻译安装为两阶段提交（先下载后解压），防止失败时产生残留文件
- 新增DownloadXUnityArchiveAsync和DownloadTranslationArchiveAsync方法实现内存下载
- 修复禁用Mod文件检测，仅包含根目录DLL文件，跳过子目录资源文件
- 新增ModInfoDumper硬件信息收集功能（CPU、内存、显卡），使用System.Management
- 新增Icons.xaml资源字典，包含对话框、标题栏和通用UI图标
- 在App.xaml中添加Icons.xaml到合并字典
- 更新国际化字符串支持新功能

### v1.3.3
#### feat: 发布1.3.3正式版，新增已安装页新上架Mod横幅、导航服务重构与翻译备份后缀迁移
- 版本升级至1.3.3
- 新增已安装页新上架Mod横幅显示，支持跳转到Mod浏览页
- 新增PageNavigationRequested事件及NavigateToPage等页面导航方法
- 新增GoToModBrowser国际化字符串用于横幅按钮
- 新增ShowUninstalledOnly字段，持久化Mod浏览页筛选状态
- 同步新上架Mod横幅数据从ModBrowserViewModel到InstalledModsViewModel
- 重构GoToInstalledMods和GoToTranslationManagement改用NavigationService
- 迁移翻译插件备份后缀从.dllbak改为.GHPCMMBAK，加载时自动迁移旧文件
- 新增旧版.dllbak备份后缀的向后兼容检测
- 修复下载进度百分比上限为100%，防止Content-Length不准确导致超限
- 修复配置注释解析，以#开头的行均视为注释
- 移除App.xaml.cs和MainViewModel中的ITranslationBackupService依赖
- 更新新上架Mod预览列表，改为显示全部检测到的Mod名称而非仅限3个

### v1.3.2
#### feat: 发布1.3.2正式版，新增多格式压缩包支持、新上架Mod横幅与管理器版本要求检查
- 版本升级至1.3.2
- 新增SharpCompress包支持多种压缩格式解压（RAR、7z、TAR、GZ、BZ2、XZ）
- 新增ExtractArchiveAsync通用解压方法，统一处理多种压缩格式
- 重构Replace安装模式，改用SharpCompress处理压缩文件
- 新增IModCatalogStateService服务，持久化Mod目录状态快照
- 新增新上架Mod检测功能，在浏览页显示横幅提示
- 新增RequiredManagerVersion字段，支持指定最低管理器版本要求
- 新增MeetsRequiredVersion方法检查版本是否满足要求
- 安装/更新/重装Mod前新增管理器版本要求检查
- 新增GoToSettingsCancel对话框按钮类型
- 窗口标题栏显示短git hash（如v1.3.2 (abc1234)）
- 清理未使用的国际化字符串，统一字符串键名
- 调整MainView.xaml中overlay层级顺序

### v1.3.1
#### feat: 发布1.3.1正式版，新增旧安装检测、备份清理重构与移除Scripted模式
- 版本升级至1.3.1
- 新增PreviousInstallationService，通过注册表追踪用户上次安装位置
- 新增首次运行时的旧安装检测对话框，提供"打开目录"和"忽略"选项
- 新增MessageDialog OpenFolderIgnore按钮类型
- 新增CommandLineArgs静态类替代DevMode，统一管理命令行参数解析
- 移除已废弃的Scripted安装模式及相关代码
- 移除DevMode.cs文件，功能迁移至CommandLineArgs.cs
- 清理NetworkService中未使用的分块下载和缓存方法
- 清理MainViewModel中未使用的ConfigurationItem类
- 移除TranslationManagerService中的重复日志调用
- 修复日志文件日期解析，改用文件名解析替代不可靠的GetCreationTime
- 修复Mod启用时文件覆盖问题，用Copy+Delete替代Move
- 新增清单迁移备份恢复机制，提高迁移安全性
- 新增残留备份目录清理逻辑，清理无清单记录的disabled目录
- 优化备份清理逻辑，清单丢失时保留手动Mod备份
- 新增ProcessService IDisposable实现，正确释放计时器资源
- 调整主界面布局，优化状态栏显示
- 调整设置页面布局，增加字段间距
- 简化翻译页面布局，移除顶部工具栏
- 新增旧安装检测和备份清理相关国际化字符串
- 移除Scripted模式相关废弃国际化字符串
- 更新完整性检查提示文本，建议"卸载重装"

### v1.3.0
#### feat: 发布1.3.0正式版，包含游戏版本检测重构、UI全面重构、Replace安装模式、完整性检查、自定义标题栏、MessageDialog系统与Mod信息导出工具
- 版本从1.2.4-beta.1经1.3.0-beta.1升级至1.3.0正式版
- 重构游戏版本检测：先从sharedassets0.assets读取（无需MelonLoader），后迁移至从globalgamemanagers读取
- 新增MelonLoader日志fallback机制，assets方法失败时回退读取日志
- 新增日期格式版本号正则匹配，后更新为完整格式匹配（如0.1.0-alpha+20260319.1）
- 新增更新下载文件大小和摘要校验
- 重构主题系统，新增Foundation基础设计令牌（字体、字号、间距、圆角、阴影）
- 新增PageStyles.xaml页面级样式，重构ControlStyles.xaml控件样式
- 全面重构各页面XAML，优化布局和视觉样式
- 新增自定义窗口标题栏，使用WindowChrome及WindowTitleBar控件（含最小化/最大化/关闭按钮）
- 实现WM_GETMINMAXINFO消息钩子，正确处理最大化窗口尺寸
- 新增Replace安装模式及ModManagerService.Replace.cs，支持直接替换游戏文件
- 新增InstalledFileInfo结构化文件信息，包含SHA256哈希和文件大小
- 安装清单SchemaVersion升级至v2，向后兼容旧版本
- 新增托管Mod完整性检查，支持缺失和修改文件检测
- 新增下架Mod支持，列表中隐藏但已安装时启动警告
- 新增状态横幅显示下架Mod和未知字段警告
- 新增未知配置字段检测，支持向前兼容
- 安装/更新Mod前新增游戏版本兼容性检查
- 增强Dev模式，支持通过-dev:"path"或-dev="path"指定自定义主配置
- 优化公告窗口，支持富文本和交互式元素
- 新增MessageDialog系统替代MessageBox，包含MessageDialogHelper静态类（Show/Confirm/ShowWarning等方法）、IDialogService/DialogService依赖注入支持及按钮/图标枚举类型定义
- 替换所有MessageBox.Show调用为MessageDialogHelper
- 新增ModInfoDumper工具，包含CopyModInfo命令（复制Mod列表及SHA256到剪贴板）和PackAllInfo命令（打包诊断信息ZIP含日志和配置）
- 新增游戏版本检测、完整性检查、下架Mod、脚本执行、ModInfoDumper及MessageDialog功能相关国际化字符串

### v1.2.3
#### feat: 发布1.2.3正式版，新增GitHub API Token加密存储、公告追踪、启动Mod更新检查与网络检测重构
- 版本升级至1.2.3正式版（从beta.2转正）
- 新增SecureStorageService，使用Windows DPAPI加密敏感数据
- 实现GitHub API Token加密存储，自动从明文迁移
- 新增UnprotectWithMigrationDetection方法，检测并迁移旧版明文Token
- 新增公告MD5追踪，识别新公告并跳过已读内容
- 公告窗口新增"更新前不再显示"复选框
- 设置页面新增"显示公告"按钮，支持手动查看
- 配置Token或代理时启动自动检查已安装Mod更新
- 首次运行时跳过主配置加载和版本清理，避免触发GitHub API
- 拆分网络连通性检测为主配置检测与GitHub API检测
- 优化主配置连通性测试，遍历所有fallback候选地址
- 新增TestConnectionAsync辅助方法，支持代理的GitHub连通性测试
- 安装向导改用CheckGitHubConnectionAsync进行网络检查
- 安装向导网络检测重构为三阶段流程：主配置连通性测试、代理列表更新、GitHub连通性测试
- 步骤2必须完成网络检测且GitHub连通性测试通过才能继续
- 新增主配置连通性测试模型与方法
- ModViewModel属性改为通知属性，支持UI自动更新
- 修复CanUpdate版本比较逻辑，统一去除v前缀
- 新增Mod重新安装命令
- 新增GitHub API Token权限提示（仅需public_repo权限）
- 翻译资源更新检查优化，Token或代理用户强制刷新
- 新增网络检测、公告、Mod更新检查相关国际化字符串

### v1.2.2
#### feat: 发布1.2.2正式版，新增MOD配置增强与安装向导优化
- 版本升级至1.2.2正式版（从1.2.1稳定版）
- 新增MOD配置多选类型支持，输出TOML数组格式
- 新增单选配置类型支持，支持本地化选项标签
- 新增MOD配置重置功能，可清除MelonPreferences.cfg中的配置段
- 新增"重新下载并安装"按钮，已有备份时可强制重新下载
- 新增下载文件校验，支持预期大小和摘要验证
- MOD详情页新增手动安装MOD卸载按钮
- 优化备份状态同步，仅显示最新版本的备份状态
- 安装向导中GitHub代理设置仅对中文用户显示
- 网络帮助按钮仅对中文用户显示
- 简化安装向导流程，所有用户都经过网络检查步骤
- 新增MelonLoader版本列表加载失败提示与重试提示
- 新增中文语言可见性转换器用于语言特定UI元素
- 新增配置重置与MelonLoader加载警告的国际化字符串

### v1.2.1
#### feat: 发布1.2.1正式版，新增DNS over HTTPS支持
- 版本升级至1.2.1正式版（从beta.1稳定版）
- 新增DoH连接器服务，支持多端点自动fallback
- 实现6个预设DoH节点（223.5.5.5、1.12.12.12、223.6.6.6、120.53.53.53、doh.apad.pro、v.recipes）
- 新增TTL缓存机制（30秒-10分钟）
- DoH失败时自动回退到系统DNS
- 重构HttpClient配置，使用统一默认配置
- 使用SocketsHttpHandler替代HttpClientHandler提升性能
- 通过ConnectCallback透明集成DoH解析
- 新增非GitHub资源的会话内存缓存
- Mod配置使用会话缓存避免重复请求
- 新增会话缓存清除方法，手动刷新时自动清除
- 设置页面新增DoH开关（仅中文用户可见）
- 修复启动时游戏运行状态未同步问题
- 新增会话缓存清除提示国际化字符串

### v1.2.0
#### feat: 发布1.2.0正式版，重构模块化UI导航与增强MelonLoader管理
- 将MainView拆分为独立的MOD浏览、已安装MOD、MOD详情与翻译视图，优化导航结构
- 新增MainConfigService，支持远程拉取、1小时缓存与内置兜底地址，实现集中化配置管理
- 新增ModBrowserViewModel，支持Tag筛选、搜索与安装更新操作
- 新增ModDetailViewModel，展示MOD详情、依赖冲突与更新日志
- 新增InstalledModsViewModel，管理已安装MOD的启用、禁用与卸载
- 移除UnifiedManifest模型，改由MainConfigService驱动远程配置
- 新增DevMode模型，支持开发者模式本地配置覆盖
- 新增MelonLoader文件清单机制，安装时记录文件列表，卸载时精准删除，不影响用户数据目录
- 新增版本清理服务，启动时对比新旧版本ZIP自动删除遗留废弃文件
- 优化MelonLoader版本检测，优先从DLL的FileVersion读取，兜底解析Latest.log
- 新增游戏版本读取接口，从Latest.log获取当前游戏版本用于MOD浏览器兼容性展示
- 将MelonLoader未安装弹窗替换为非阻断遮罩，提供直接跳转安装的按钮
- 重构游戏运行遮罩，仅覆盖内容区域，保持状态栏停止按钮可点击
- MOD浏览器支持版本兼容性彩色标签，匹配当前游戏版本显示绿色，不匹配显示黄色
- 设置页与安装向导代理服务器选择从枚举绑定重构为对象绑定
- 进入安装向导第2步时自动从远程主配置拉取最新代理节点列表
- 依赖缺失对话框改为显示MOD名称，不再显示原始ID
- 自动更新前重置版本清理标记，确保更新后下次启动触发清理
- 主界面新增"打开游戏目录"按钮，可直接在资源管理器中打开游戏根目录
- 修复首次安装时安装向导完成后触发不必要的旧版本文件清理问题，完成安装时预写CleanupDoneForVersion跳过清理
- SetupWizardViewModel注入IUpdateService以支持版本感知的安装完成逻辑
- 补充新视图与导航标签的本地化字符串
- 发布格式改为单文件可执行，目标平台win-x64
- 升级版本至1.2.0正式版并同步更新程序集元数据

### v1.1.4

#### feat: 发布1.1.4正式版，新增MelonLoader管理功能与稳定性修复
  - 在设置页新增MelonLoader管理面板：查看已安装版本、启用/禁用及从GitHub重新安装
  - 主界面新增MelonLoader已禁用遮罩层，提示MOD操作不可用
  - 通过解析MelonLoader/Latest.log检测已安装版本号
  - 在安装向导网络配置页新增GitHub API Token输入框
  - 安装向导中强制代理与Token互斥：启用代理时清空Token，反之亦然
  - 修复游戏运行检测时机，改为下载完成后检查，避免文件写入冲突
  - 修复MOD文件匹配逻辑，改用精确文件名比较替代部分匹配
  - 修复备份还原以支持backup_paths.json路径映射并检测空备份
  - 修复备份目录清理，改为递归删除含backup_paths.json的残留文件
  - 修复MOD排序，未安装MOD改为保持JSON原始顺序而非字母排序
  - 修复加载时清单保存改用await而非即发即忘
  - 升级版本至1.1.4并更新程序集元数据

### v1.1.3-beta.1

#### feat: 发布1.1.3-beta.1测试版本，新增GitHub API Token支持与并行加载优化
  - 新增GitHub API Token认证功能，突破频率限制（60→5000请求/小时）并自动直连
  - 优化MOD加载流程，并行获取GitHub版本信息以缩短启动时间
  - 并行化版本更新检查，加速所有MOD的刷新速度
  - 修复备份文件名匹配逻辑，从备份路径中提取原始文件名
  - 修复手动安装MOD的IsSupportedManualMod标记
  - 新增翻译提示面板，警告FPS影响与快捷键冲突
  - 配置GitHub Token时自动禁用代理设置以确保直连API
  - 升级版本至1.1.3-beta.1并更新程序集元数据

### v1.1.2

#### feat: 发布1.1.2正式版，优化导航单例模式与资源重新生成
  - 将MainViewModel与MainView改为单例生命周期，避免导航时重新创建
  - 包含了1.1.2-beta.1的修改内容

### v1.1.2-beta.1

#### feat: 发布1.1.2-beta.1测试版本，新增离线模式、启动检查与MOD更新日期显示
  - 引入离线模式，网络不可用时优雅降级，允许本地操作但阻止安装更新
  - 新增启动前冲突与依赖验证，通过确认对话框防止运行时问题
  - 显示MOD更新日期，采用相对时间格式（今天/昨天/X天前）并附版本号
  - 清理时保留已禁用MOD备份，仅删除已卸载备份以保持回滚能力
  - 优化GitHub频率限制提示，建议切换代理服务器
  - 简化.gitignore，移除AI助手文件排除规则
  - 升级版本至1.1.2-beta.1并更新程序集元数据

### v1.1.1

#### feat: 发布1.1.1正式版，新增Steam自动搜寻与翻译体验升级
  - 引入SteamGameFinderService搭配向导自动搜寻GHPC路径并提示非Steam版本
  - 优化翻译更新体验，加入实时进度、UTC清单时间与新版按钮样式
  - 下调多线程下载阈值并补充自动化相关本地化字符串
  - 发布稳定版v1.1.1，更新程序集元数据与资源文本

### v1.1.1-beta.1

#### feat: 发布1.1.1-beta.1测试版本，新增BepInEx检测与界面增强
  - 新增BepInEx检测逻辑，防止与现有安装冲突
  - 引入布尔值AND转可见性转换器，支持复杂UI绑定场景
  - 更新版本至1.1.1-beta.1，集成WebView2依赖
  - 增强字符串资源与本地化基础设施
  - 改进网络服务稳定性与错误处理
  - 优化翻译管理器与更新服务可靠性

### v1.1.0

#### feat: 发布1.1.0正式版，优化翻译体验与更新流程并强化多线程下载
  - 新增语言显示转换、智能窗口尺寸与中文社区快捷操作
  - 限制手动翻译管理、本地化提示并避免重复启动更新检查
  - 重构模组与应用更新检测，复用GitHub API地址并支持语义化版本比较
  - 增强IDM风格下载引入工作窃取并扩展日志本地化文本

### v1.1.0-beta.1

#### feat: 发布1.1.0-beta.1测试版本，新增应用内更新与翻译升级
  - 更新系统：稳定测试更新通道选择，支持后台检查与一键更新安装
  - 检测手动翻译安装，跟踪版本时间戳，并在界面提示可用更新
  - 重构下载流程，采用IDM风格分块下载并限制提醒
  - 扩展界面：更新提示条、设置检查按钮、日志筛选导出、更大布局与文案更新

### v1.0.1

#### feat:发布1.0.1正式版，增强文件追踪和翻译管理
  - 加全面的文件操作追踪系统
  - 实现翻译插件管理的启用/禁用功能
  - 增强网络连接测试的代理和直连功能
  - 改进模组安装过程的文件操作追踪
  - 添加翻译备份服务和统一清单支持
  - 更新资源字符串与新翻译条目
  - 增强手动模组的卸载/重装功能
  - 更新版本到1.0.1正式版

### v1.0.0

#### feat: 发布1.0.0正式版，改进本地化和系统增强
  - 添加模组更新检查功能
  - 改进资源字符串组织和新增条目     
  - 改进日志系统使用本地化消息
  - 重构主题初始化和颜色处理
  - 更新版本到1.0.0正式版

### v1.0.0-beta.3

#### feat: 添加公告系统并改进应用稳定性
- 添加公告服务用于Markdown内容显示
- 添加带有适当样式的公告窗口UI
- 改进应用程序关闭时的资源清理
- 修复GitHub工作流
- 增强主窗口尺寸设置(1280x720)
- 添加UI绑定的值转换器
- 更新模组视图模型的新属性
- 添加完整的字符串资源
- 更新版本至1.0.0-beta.3
- 添加Markdig包用于markdown渲染

### v1.0.0-beta.2-hotfix1

#### hotfix: 改进模组安装以处理压缩包和DLL文件
- 添加代理服务器选择枚举
- 增强NetworkService支持可配置代理域名
- 改进模组安装以处理压缩包和DLL文件
- 修复脚本安装传递下载文件路径而非URL
- 在TranslationManagerService中添加git克隆代理支持
- 更新UI在设置中显示代理服务器选择下拉框
- 重新排序设置向导步骤（语言选择优先）
- 版本号升级至1.0.0-beta.2-hotfix1

### v1.0.0-beta.2

#### feat: 添加模组备份系统并改进模组管理功能
- 添加模组自动备份/恢复服务
- 实现模组安装的依赖和冲突检查
- 添加GitHub页面导航和游戏目录访问功能
- 改进资源管理并增强字符串转换器
- 为新功能添加全面的本地化支持
- 更新版本至1.0.0-beta.2