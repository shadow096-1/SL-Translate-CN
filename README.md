# SL-Translate-CN

LabAPI 中文聊天插件，为 SCP: Secret Laboratory 的玩家客户端控制台添加三个命令，并在消息中显示发送者阵营、存活状态和角色：

- `.bc <内容>`：公屏说话，默认广播/提示显示 10 秒。
- `.c <内容>`：阵营频道，只发送给同阵营玩家。
- `.ac <内容>`：举报频道，私信给在线 Remote Admin 管理，并写入服务器日志。

## 构建

```bash
dotnet build SL-Translate-CN.sln -c Release
```

构建后将 `SLTranslateCN.dll` 放入服务器的 `LabAPI/plugins/<端口>` 或 `LabAPI/plugins/global` 目录。

## 配置

插件会读取 `sl_translate_cn.yml`，可配置是否启用、各频道显示时长，以及是否向客户端控制台发送纯文本副本。
