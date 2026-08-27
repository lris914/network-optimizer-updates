<!-- sparkle-sign-warning:
IMPORTANT: This file was signed by Sparkle. Any modifications to this file requires updating signatures in appcasts that reference this file! This will involve re-running generate_appcast or sign_update.
-->
# 网络优化器 V4.6.0

本版本把网络优化器升级为可信状态监控与本地网络优化优先。

- 递归展示规则模式、自动策略组与活动叶节点，不再把 GLOBAL=DIRECT 直接判为 VPN 故障。
- 海外探测采用预热、多端点三轮样本、中位数与 P95；部分端点失败单独标记不确定。
- 地区选择改为监控偏好，主页与设置同步；偏好不同不污染总体健康。
- 刷新严格只读；节点操作降级到高级修复，本地网络优化保持主要操作。
- macOS 与 Windows 主页在 980×680 下保持核心任务一屏可达。
