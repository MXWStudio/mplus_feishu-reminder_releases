# M+ 应用下载

本仓库只存放应用安装包、校验文件与使用说明，不包含私有工程源码或业务运行数据。

## 飞书表格中枢

下载 [M+飞书表格中枢 0.11.0](https://github.com/MXWStudio/mplus_feishu-reminder_releases/releases/tag/hub-v0.11.0)。

- 适用系统：Windows x64。
- 安装包：`MPlus-Feishu-Hub-Setup-0.11.0-x64.exe`。
- 安装包目前未签名，不提供应用内自动更新。Windows 可能提示未知发布者。
- 安装结束不自动运行。请在原采集应用退出后手动启动，避免同一业务使用两个采集节点。
- Chrome 加载安装目录 `resources/collector-extension`，再通过控制台完成配对。
- 凭据与运行数据由使用者在本机单独配置，不随应用分发。
- 具体步骤见 [安装与使用](INSTALL.md)。

`hub-v*` 是飞书表格中枢版本。旧 `v0.10.x` 为 M+提醒历史版本，保留原安装文件及更新元数据。

## 校验下载

下载同一版本的 `SHA256SUMS.txt`，在 PowerShell 中运行：

```powershell
Get-FileHash .\MPlus-Feishu-Hub-Setup-0.11.0-x64.exe -Algorithm SHA256
```

结果应与校验文件内对应文件的 SHA-256 一致。
