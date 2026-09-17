# M+ 应用下载

本仓库提供应用安装包、校验文件与安装说明，不包含私有工程源码、登录凭据或业务运行数据。

## M+控制台 0.11.3

[下载 Mac / Windows 安装包](https://github.com/MXWStudio/mplus_feishu-reminder_releases/releases/tag/hub-v0.11.3)

| 系统与芯片 | 安装包 |
| --- | --- |
| Windows x64 | `m-plus-feishu-reminder-0.11.3-windows-x64-setup.exe` |
| Mac Apple Silicon（M 系列） | `m-plus-feishu-reminder-0.11.3-macos-arm64.dmg` |
| Mac Intel | `m-plus-feishu-reminder-0.11.3-macos-x64.dmg` |

Mac 同时提供 ZIP。Mac 最低系统要求为 macOS 12；本版使用 macOS 15 构建验证。Windows 使用 Windows Server 2022 构建验证，并已完成 Windows 11 本机安装运行验证。

- 用途：只读采集 M+ 数据，在本机保存、核对后同步到飞书，并按已配置的通知群处理日报。
- 本版改善采集恢复和状态提示，支持迁移浏览器采集进度、每日加密备份，并修复 Windows 文件短暂被占用导致状态保存失败的问题。
- 已有用户升级前从托盘退出原应用。新安装建议统一放在 `D:\mplus_feishu\app`，桌面入口为“M+控制台”。
- Windows 包未做发行者签名；Mac 包仅有临时完整性签名，没有 Developer ID 签名及 Apple 公证。不提供应用内自动更新。凭据、浏览器登录和业务配置由使用者在本机设置。
- 具体操作见 [安装与使用](INSTALL.md)。

`hub-v*` 是 M+控制台（飞书表格中枢）版本。旧 `v0.10.x` 为 M+提醒历史版本，保留原安装文件和更新元数据；请勿将两种应用混装。

## 校验下载

下载同一版本的 `SHA256SUMS.txt`，在 PowerShell 中运行：

```powershell
Get-FileHash .\m-plus-feishu-reminder-0.11.3-windows-x64-setup.exe -Algorithm SHA256
```

Mac 可使用 `shasum -a 256 文件名`。结果应与校验文件中对应文件的 SHA-256 一致。

每版使用 `hub-v版本号` 标签，附中文更新说明、安装升级指南、校验文件和各平台 `build-info`。文件名区分平台与芯片，发布后不覆盖原文件；修复另发版本。
