<div align="center">
  <img src="assets/network-optimizer-icon.png" width="150" alt="网络优化器图标">
  <h1>网络优化器</h1>
  <p><strong>面向 macOS 的 Clash Verge / Mihomo 网络诊断与日本节点智能恢复工具</strong></p>
  <p>自动发现真实代理端口，持续监测网络状态，并在异常时安全恢复现有连接。</p>

  <p>
    <a href="https://github.com/lris914/network-optimizer-updates/releases/latest">
      <img src="https://img.shields.io/badge/下载最新版-前往%20Releases-1677ff?style=for-the-badge&logo=github" alt="下载最新版">
    </a>
  </p>

  <p>
    <img src="https://img.shields.io/badge/macOS-13%2B-111111?style=flat-square&logo=apple" alt="macOS 13+">
    <img src="https://img.shields.io/badge/架构-Apple%20Silicon%20%7C%20Intel-4c8bf5?style=flat-square" alt="Universal">
    <img src="https://img.shields.io/badge/当前版本-V3.3.2-20a464?style=flat-square" alt="V3.3.2">
    <img src="https://img.shields.io/badge/界面-简体中文-f59e0b?style=flat-square" alt="简体中文">
  </p>
</div>

---

## 它能做什么

- 自动发现 Clash Verge Rev / Mihomo 的本机控制接口、实时代理端口和策略组。
- 分别检测国内基础网络与海外代理链路，避免把 Clash 故障误报为网络正常。
- 只在用户现有订阅中识别日本候选节点，不读取或修改订阅地址。
- 当前节点异常时进行独立确认，并选择当前质量更合适的日本节点。
- Clash Verge 未启动或控制接口持续异常时，可受限地启动或重启应用。
- 支持低资源后台监测、macOS 系统通知和可试听的系统原生提示音。
- 提供基于 macOS `networkQuality` 的本地网络测速。

## 下载与安装

点击下面的入口进入 GitHub Releases 下载最新版 DMG：

### [下载网络优化器](https://github.com/lris914/network-optimizer-updates/releases/latest)

1. 下载最新版 `.dmg`。
2. 打开 DMG，将“网络优化器”拖入“Applications（应用程序）”。
3. 覆盖升级时，在 macOS 提示中选择“替换”。
4. 当前版本尚未使用 Apple Developer ID 公证。首次打开如被拦截，请在 Finder 中右键应用并选择“打开”。

应用名称和 Bundle ID 保持固定，覆盖升级不会主动删除原有网络优化器设置。

## 安全边界

- 只访问本机回环接口或本机 Unix Socket。
- 不读取、上传、刷新或改写代理订阅。
- 不修改 DNS、TUN、路由、规则或 macOS 系统代理。
- 不扫描局域网，不下载或替换 Mihomo 内核。
- 不静默选择非日本节点。
- 控制密钥只保存在当前用户的 macOS 钥匙串中。

## 系统要求

- macOS 13 或更高版本。
- Apple Silicon 或 Intel Mac。
- 已安装并配置 Clash Verge Rev，或其他提供标准 Mihomo 本机控制接口的客户端。

## 关于这个仓库

本仓库只用于发布网络优化器的安装包、版本说明和后续在线更新清单，不公开应用源代码。

当前 V3.3.2 使用手动下载安装。后续版本将逐步加入应用内检查、下载和覆盖更新能力。

---

<div align="center">
  <sub>网络优化器 · 简洁、受限、可回滚的本机网络恢复工具</sub>
</div>
