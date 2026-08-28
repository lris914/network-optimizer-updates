<!-- sparkle-sign-warning:
IMPORTANT: This file was signed by Sparkle. Any modifications to this file requires updating signatures in appcasts that reference this file! This will involve re-running generate_appcast or sign_update.
-->
# 网络优化器 V4.6.1

本版本重点修复偶发状态误报，并简化设置保存流程。

- 基础网络、控制接口、代理端口、代理出口、地区偏好与数据新鲜度分别判断；地区偏好不同只作提示。
- 控制接口发现加入启动宽限、连续三次失败确认与最近有效状态保留；单次波动不会立即清空端口、策略组或节点。
- 只读刷新继续禁止切换节点、重启客户端或修改配置；过期检测结果不能覆盖较新的状态。
- 新安装默认关闭提示音，系统通知保持独立；升级不会覆盖旧用户已明确保存的声音选择。
- 设置页统一为一个“保存”主操作；连接设置先校验，成功后提交，失败时保留原设置并说明原因。
