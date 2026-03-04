# OpenClaw Windows 一键部署与升级指南

本文档介绍了如何在 Windows 环境下使用提供的批处理脚本实现 OpenClaw 的一键本地部署、运行以及打包升级。

## 1. 一键启动 OpenClaw

**使用方法：** 右键管理员运行 `start_gateway.bat`。

<img width="735" height="324" alt="image" src="https://github.com/user-attachments/assets/7cc5b814-a940-4d9c-9ab6-901c4cc44300" />

等待出现日志即可访问：

```
[OpenClaw] Starting via local Node.js...
Base: "C:\Users\1\Downloads\OpenClaw"
Node: "C:\Users\1\Downloads\OpenClaw\node-v22.22.0-win-x64\node.exe"

🦞 OpenClaw  2026.2.26 (bc50708) — Chat automation for people who peaked at IRC.

23:10:48 [canvas] host mounted at http://127.0.0.1:18789/__openclaw__/canvas/ (root C:\Users\1\Downloads\OpenClaw\data\canvas)
23:10:50 [heartbeat] started
23:10:50 [health-monitor] started (interval: 300s, grace: 60s)
23:10:50 [gateway] agent model: openai/qwen-plus
23:10:50 [gateway] listening on ws://127.0.0.1:18789, ws://[::1]:18789 (PID 35856)
23:10:50 [gateway] log file: \tmp\openclaw\openclaw-2026-03-05.log

```



**访问浏览器**：http://localhost:18789/chat?token=ef9f6edea733b0330b917c2117a0f25417552f8398c23e10



## 2. 运行openClaw命令

**使用方法：** 右键管理员运行 双击运行 `openclaw_cmd.bat`。

提示输入选项，比如`onboard`：

```
Input OpenClaw command args, e.g. onboard: onboard
```



## 3. 修改大模型配置

**使用方法：** 右键管理员运行 双击运行 `openclaw_cmd.bat`。输入onboard，进行初始化配置，或者修改`C:\Users\1\Downloads\OpenClaw\data\openclaw.json`

## 4. 一键打包与发布 (备份)

**使用方法：** 右键管理员运行 `pack_release.bat`。



---
*提示：所有运行产生的日志和系统反馈都会直接在终端黑窗口中输出展示。如果发生闪退无法看清报错，建议您在此目录下打开 CMD 或 PowerShell 窗口，将 `.bat` 文件直接拖进去回车运行来进行排障。*
