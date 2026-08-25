<!-- sparkle-sign-warning:
IMPORTANT: This file was signed by Sparkle. Any modifications to this file requires updating signatures in appcasts that reference this file! This will involve re-running generate_appcast or sign_update.
-->
# 网络优化器 V4.5.2

这是一个 macOS 图标尺寸兼容修复版本。

- 图标主体统一缩放到 824×824 标准安全区。
- 1024×1024 母版四周各保留 100 px 真透明边距。
- 修复 macOS 15.7.9 启动台中图标比其他应用偏大的问题，同时保持较新系统中的视觉尺寸一致。
- 构建门禁新增可见图形边界检查。
- Windows 版本号同步更新，功能行为保持 V4.5.0 不变。

macOS 在线更新会验证 Sparkle EdDSA 签名。Windows 发布包已通过 NuGet 已知漏洞检查与 Microsoft Defender 扫描；未购买商业代码签名，仍可能出现“未知发布者”提示。
