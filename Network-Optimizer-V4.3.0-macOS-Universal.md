<!-- sparkle-sign-warning:
IMPORTANT: This file was signed by Sparkle. Any modifications to this file requires updating signatures in appcasts that reference this file! This will involve re-running generate_appcast or sign_update.
-->
# 网络优化器 V4.3.0

- macOS 与 Windows 的本地网络优化升级为三轮综合评估。
- 每个 DNS 解析器跨三个域名采集 9 次结果，优先比较成功率，再比较中位延迟与抖动。
- 带宽测速仍只执行一次，避免多轮分析产生三倍流量。
- MTU 探测与 DNS 分析并行执行，结果仍只作为建议，不会自动修改系统网络配置。

