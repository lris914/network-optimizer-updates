<!-- sparkle-sign-warning:
IMPORTANT: This file was signed by Sparkle. Any modifications to this file requires updating signatures in appcasts that reference this file! This will involve re-running generate_appcast or sign_update.
-->
# 网络优化器 V4.5.4

这是一次 Clash Verge Rev 本地配置兼容修复。

- 支持从 Mihomo 启动参数发现 Unix Socket 控制接口，不再把 Clash Verge 界面端口当作控制 API。
- 从运行配置读取实际 Mixed/HTTP/SOCKS 端口和通用策略组。
- 支持单节点、本地配置和多地区节点；所选地区缺少候选时给出准确提示。
- 节点名称没有地区时，仅在两个独立出口国家信号一致时使用回退。
- Windows 同步版本号，既有功能行为不变。
