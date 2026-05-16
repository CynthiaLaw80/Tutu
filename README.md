# Tutu: 智能大学生职业规划玩偶

本项目旨在开发一款基于 ESP32-S3 的智能玩偶，集成 ASR/LLM/TTS 技术，实现语音交互、心理咨询及职业规划建议功能。

## 🚀 团队分工

- **Member A (硬件工程师)**: 原理图设计、电路搭建、功放与麦克风调试、物理结构封装。
- **Member B (系统集成/技术组长)**: ESP32 固件开发 (I2S/Wi-Fi/WS)、APP 通信中台逻辑、全链路联调。
- **Member C (AI/后端工程师)**: 云端 API 部署、ASR/LLM/TTS 算法选型与 Prompt 优化。
- **Member D (UI/UX 工程师)**: APP 界面开发、SQLite 本地历史记录存储、交互动画。

## 📂 目录结构

```text
/Tutu
  ├── /Hardware           # Member A: 原理图PDF、电路图、物料清单
  ├── /Firmware           # Member B: ESP32-S3 代码 (Arduino)
  ├── /App                # APP 源码
  │    ├── /lib/network   # Member B: 通信逻辑
  │    └── /lib/ui        # Member D: 界面与本地数据库
  └── /Backend            # Member C: 云端Python后端代码
```

## 🛠 开发注意事项

**代码提交**:

- 提交前请先 `git pull` 远程代码，防止冲突。
- Commit 信息格式：`[姓名] 描述` (例如: `[Member D] 实现在 APP 本地 SQLite 存储对话记录`)。

**分支管理**：

- 不要直接改 main 分支。每个人建立自己的分支（如 dev-hardware, dev-app-ui, dev-app-network, dev-firmware, dev-backend），功能写完后，由 B 统一合并。
- 给 C 的建议： 你的 API 地址如果变了，及时更新工程根目录下的 config.json 或 README，方便 B 修改。
- 给 D 的建议： 本地数据库字段要预留好（id, role, content, time, audio_path），方便 B 调用。

---
