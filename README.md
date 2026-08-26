<div align="center">
  <img src="assets/network-optimizer-icon.png" width="144" alt="网络优化器图标">
  <h1>网络优化器 V4.5.3</h1>
  <p><strong>面向 macOS 与 Windows 的 Mihomo / Clash 网络诊断、地区优选与自动恢复工具</strong></p>
  <p>自动发现本机控制端口和订阅节点地区，只在你选择的地区内检测、优选并恢复代理连接。</p>

  <p>
    <a href="https://github.com/lris914/network-optimizer-updates/releases/latest">
      <img src="https://img.shields.io/badge/下载最新版-网络优化器%20V4.5.3-1677ff?style=for-the-badge&logo=github" alt="下载网络优化器 V4.5.3">
    </a>
  </p>

  <p>
    <img src="https://img.shields.io/badge/macOS-13%2B-111111?style=flat-square&logo=apple" alt="macOS 13+">
    <img src="https://img.shields.io/badge/Windows-10%20%7C%2011-0078d4?style=flat-square&logo=windows11" alt="Windows 10/11">
    <img src="https://img.shields.io/badge/架构-Universal%20%7C%20x64%20%7C%20ARM64-4c8bf5?style=flat-square" alt="支持架构">
    <img src="https://img.shields.io/badge/当前版本-V4.5.3-20a464?style=flat-square" alt="V4.5.3">
  </p>
</div>

---

## V4.5.3 更新

- 区分本地断网、证据不足、当前节点异常和候选池大面积不可用，故障提示更明确。
- 刷新状态会并发执行一次轻量本地测速，避免重复初始化和串行等待。
- 自动恢复采用可取消、带退避的周期复测；只有启用自动恢复时才允许切换节点，关闭时只给诊断和推荐。
- 成功切换后回读实际生效节点，再原子更新“当前节点”；失败或回滚不会误报成功。
- Windows 联网检测使用四个唯一国内/全球主机并验证预期响应，避免全球端点不可达时误报整机断网。
- Windows 主页在 1120×760 和 980×680 下无需强制纵向滚动；ARM64 实机与 x64/ARM64 制品均完成发布验收。

## 平台功能

| 功能 | macOS | Windows |
|---|---|---|
| 系统与架构 | macOS 13+，Apple Silicon / Intel Universal | Windows 10/11，x64 / ARM64 |
| 控制接口 | Unix Socket、本机 TCP | 本机 TCP |
| 客户端识别 | Nano、Clash Verge Rev、Clash Party、FlClash、Clash Nyanpasu、ClashX 系列 | Nano、Clash Verge Rev、Clash Party、FlClash、Clash Nyanpasu、Clash for Windows 兼容模式 |
| 地区与节点 | 多地区分类、严格筛选、最优节点与失败回滚 | 多地区分类、严格筛选、最优节点与失败回滚 |
| 后台监测 | LaunchAgent、系统通知、系统提示音 | 系统托盘、Windows 通知与系统提示音 |
| 本地网络优化 | 原生下载/上传测速、DNS/MTU 应用、自动复测与回滚 | 轻量下载/上传测速、DNS/MTU 应用、自动复测与回滚 |
| 软件更新 | Sparkle EdDSA 签名检查、下载与确认安装 | 检查 GitHub Releases，并匹配当前架构安装包 |

## 下载与安装

### macOS

- [下载 Universal DMG 安装包](https://github.com/lris914/network-optimizer-updates/releases/download/v4.5.3/Network-Optimizer-V4.5.3-macOS-Universal-Installer.dmg)
- [下载 Universal ZIP 更新包](https://github.com/lris914/network-optimizer-updates/releases/download/v4.5.3/Network-Optimizer-V4.5.3-macOS-Universal.zip)

打开 DMG，将“网络优化器”拖入“Applications（应用程序）”。覆盖旧版时选择“替换”，原有设置会保留。当前安装包使用临时应用签名，没有 Apple Developer ID 公证。

### Windows

- [下载 Windows x64 版本](https://github.com/lris914/network-optimizer-updates/releases/download/v4.5.3/Network-Optimizer-V4.5.3-Windows-x64.zip) — 绝大多数 Intel / AMD 电脑
- [下载 Windows ARM64 版本](https://github.com/lris914/network-optimizer-updates/releases/download/v4.5.3/Network-Optimizer-V4.5.3-Windows-ARM64.zip) — Snapdragon 等 ARM Windows 电脑

解压后运行 `NetworkOptimizer.exe`。当前版本没有商业代码签名，Windows 可能显示“未知发布者”。

## 工作方式

1. 启动用户自己的兼容代理客户端。
2. 网络优化器验证 `/version`、`/configs` 和 `/proxies`，识别真实控制接口、代理端口与策略组。
3. 软件根据节点名称、地区代码和国旗文本分类当前订阅实际存在的地区。
4. 用户选定地区后，检测、排序、切换和自动恢复都严格限制在该地区。
5. 当前节点异常时进行多端点确认，再按成功率、可靠性、延迟、抖动和近期失败记录选择候选。
6. 切换失败会恢复原选择链并进入退避，不会静默改用其他地区。

## 安全与隐私边界

- 只访问本机回环接口或本机 Unix Socket。
- 不读取、上传、刷新或改写代理订阅。
- 只有用户点击应用或恢复按钮并通过系统管理员确认后，才会修改当前活动网卡的 DNS/MTU；不修改 TUN、路由、规则或系统代理。
- 不扫描局域网，不下载或替换 Mihomo 内核。
- 不选择当前所选地区以外的节点。
- 自动重启只处理当前用户的已识别客户端界面进程，不结束 Mihomo 核心或特权服务。
- macOS 控制密钥保存在钥匙串；Windows 控制密钥使用当前用户数据保护加密。

## 关于这个仓库

本仓库只提供安装包、版本说明和在线更新清单，不公开网络优化器源代码。

---

<div align="center">
  <sub>网络优化器 · 双平台、多地区、低干扰、可回滚</sub>
</div>
