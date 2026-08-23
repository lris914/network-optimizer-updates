<!-- sparkle-sign-warning:
IMPORTANT: This file was signed by Sparkle. Any modifications to this file requires updating signatures in appcasts that reference this file! This will involve re-running generate_appcast or sign_update.
-->
# 网络优化器 V4.0.0

V4.0.0 是首个 macOS 与 Windows 双平台正式版本。

## macOS 更新

- 兼容范围扩展到 Nano、Clash Verge Rev、Clash Party、FlClash、Clash Nyanpasu、ClashX / ClashX.Meta 与 ClashX Pro。
- 自动发现当前用户的 Unix Socket 或本机 TCP 控制接口，并重新读取实时代理端口和策略组。
- 自动自愈从只处理 Clash Verge 扩展为受限启动或重启当前已识别客户端的界面进程。
- 设置页统一标签、字段宽度、控件尺寸和说明层级，减少过大的输入框及不一致布局。
- 保留多地区严格筛选、后台低频监测、系统通知、原生提示音、本地网络测速和 Sparkle 签名在线更新。

## Windows 新增

- 新增 Windows 10/11 x64 与 ARM64 自包含版本，无需预装 .NET。
- 采用 Win11 Fluent/Mica 主界面与设置页，统一圆角输入框、下拉框、按钮和导航交互。
- 支持 Nano、Clash Verge Rev、Clash Party、FlClash、Clash Nyanpasu 与 Clash for Windows 兼容模式。
- 支持自动发现本机 Mihomo TCP 控制接口、真实代理端口和策略组。
- 支持地区分类、当前地区节点优选、失败回滚、低频后台监测、托盘通知和系统提示音。
- 支持检查 GitHub Releases，并识别与当前 Windows 架构匹配的安装包。

## 安全边界

- 不读取、上传、下载、刷新或修改订阅。
- 不修改 DNS、TUN、路由、规则或系统代理。
- 不扫描局域网或操作远程控制器。
- 不跨地区静默切换节点。
- 自动重启只处理已识别的客户端界面进程，不结束 Mihomo 核心或特权服务。
