<!-- sparkle-sign-warning:
IMPORTANT: This file was signed by Sparkle. Any modifications to this file requires updating signatures in appcasts that reference this file! This will involve re-running generate_appcast or sign_update.
-->
# 网络优化器 V4.4.0

- 新增优化前实测、推荐配置实测和提升量对比。
- 显示 DNS 成功率、延迟、抖动分别提升多少，以及建议改动和实际改动。
- 推荐配置尚未应用时会明确标记，不会把候选测试结果冒充为系统已经优化。
- 每次分析完成后保存 DNS 与 MTU 快照，可恢复优化前状态或系统自动配置。
- 回滚前校验活动网卡，macOS 使用管理员验证，Windows 使用 UAC。
