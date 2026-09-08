<!-- sparkle-sign-warning:
IMPORTANT: This file was signed by Sparkle. Any modifications to this file requires updating signatures in appcasts that reference this file! This will involve re-running generate_appcast or sign_update.
-->
# 网络优化器 V4.7.0


- macOS 将手动与周期刷新合并为单一只读事务；旧任务不能覆盖新结果或清理新任务句柄，主动修复前会使旧检测失效。
- 设置保存与检测互斥，异步校验在提交前完成；Windows 设置窗口打开期间暂停后台检测，减少状态交错。
- macOS 每批海外探测从七个独立会话收敛为一个，复用预热连接；两端限制最多三轮，结束后释放会话资源。
- 修复 macOS 请求耗时丢失整数秒；海外探针只接受预期 204 响应，不把登录、重定向和拒绝页当作出口正常。
- 首页状态文字、图标与颜色统一决策，旧健康快照明确显示待复核，地区偏好不参与故障判定。
- 清除无入口的旧恢复逻辑、旧结果面板和重复统计/设置复制代码；保留测速、自动恢复、设置迁移、在线更新与回滚。
- Windows 切换地区偏好只刷新状态，不额外下载/上传测速；只有实测才能声明对应网络能力。

