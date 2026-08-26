<!-- sparkle-sign-warning:
IMPORTANT: This file was signed by Sparkle. Any modifications to this file requires updating signatures in appcasts that reference this file! This will involve re-running generate_appcast or sign_update.
-->
# 网络优化器 V4.5.3

这是一次网络故障分级、恢复安全性与 Windows 可用性更新。

- 区分本地断网、证据不足、当前节点异常和候选池大面积不可用。
- 刷新状态时同步执行一次轻量本地测速，并减少串行探测和重复初始化。
- 自动恢复采用可取消、带退避的周期复测；关闭自动恢复时只诊断和推荐，不切换节点。
- 节点切换仅在回读确认实际生效后更新“当前节点”，失败或回滚不会误报成功。
- Windows 使用唯一的国内与全球联网探针，降低正常网络被误判为断网的概率。
- Windows 主页在默认窗口和 980×680 最小窗口下无需强制纵向滚动。

macOS 在线更新会验证 Sparkle EdDSA 签名。Windows ARM64 发布包已在 Windows 11 ARM64 环境真实启动并完成刷新、便携卸载和旧版回退；x64 与 ARM64 制品均通过 NuGet 已知漏洞检查和 Microsoft Defender 扫描。Windows 尚未购买商业代码签名，仍可能出现“未知发布者”提示。
