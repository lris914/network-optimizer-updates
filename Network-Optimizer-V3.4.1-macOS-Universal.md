<!-- sparkle-sign-warning:
IMPORTANT: This file was signed by Sparkle. Any modifications to this file requires updating signatures in appcasts that reference this file! This will involve re-running generate_appcast or sign_update.
-->
# 网络优化器 V3.4.1

这是一次界面一致性、在线更新体验和资源占用优化更新。

## 更新内容

- 设置窗口改用 macOS 原生侧边栏选择，页面切换范围更明确。
- 未修改设置时只显示“完成”；存在未应用修改时才显示“取消”和“应用并重新检测”。
- “恢复自动连接设置”移动到连接页面，仅恢复连接相关项目，不影响地区和通知偏好。
- 删除国旗说明、私有仓库等历史或内部描述，统一为面向所有用户的文案。
- 在线更新支持每日、每周、每两周检查，以及可选的自动下载。
- 发现新版本后显示更新说明；用户确认安装后，应用会自动替换并重新打开。
- 更新来源改为可点击的 GitHub 项目主页。
- 清理无效逻辑并压缩可执行文件，降低应用体积与空闲内存占用。

## 安装说明

下载 DMG，将“网络优化器”拖入“Applications（应用程序）”。覆盖旧版时选择“替换”，原有设置会保留。

当前安装包使用临时应用签名，没有 Apple Developer ID 公证。首次打开若被 macOS 拦截，请在 Finder 中右键应用并选择“打开”。
