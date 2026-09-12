# 霓虹破碎 v18 发布

Windows x64 和 PC Web 发布包位于 build/releases/v18，各自解压即可部署。不包含原始生成素材、服务配置或测试脚本。

- Windows：NeonBreak-v18-windows.zip，解压后运行 NeonBreak.exe，保持 PCK 在旁边。这次使用官方 release 模板，不再复制完整 Godot 编辑器作为游戏程序。
- Web：NeonBreak-v18-web.zip，部署说明见 WEB_RELEASE.md。提供 serve.py 本地 HTTP 服务与静态托管响应头示例。
- SHA256SUMS.txt、manifest.json 记录压缩包大小、哈希和源代码提交。

本次补丁：连续攻击接招前读取左右方向，允许在合法接招窗口反向出招，不再需要先停止按攻击。反向重置为起手式，当前一击的有效阶段仍固定方向。主角 HUD 姓名、血条、数值统一左边界，并给实际字体行高留出空间；头像与面板保持内边距。

Godot 4.7.2 官方模板已从 godotengine/godot-builds 下载，使用官方 SHA512-SUMS.txt 校验；Windows/Web 模板安装到用户 Godot 模板目录。没有使用 Q6，没有改动 BGM。

验证：转向边界 34 项、武器 38 项、输入/空间/战斗回归通过；Windows release EXE 使用 ANGLE 和默认音频设备启动、进入检查点并截图成功，无错误。Chrome 实际打开最终 Web 包，确认标题、对白推进、战斗及暂停响应；控制台无 error/warn。Windows 与 Web 主角 HUD 已视觉核对。

本次未验证实物手柄、Safari、移动端或公网托管平台，也没有重新跑完整通关。Web 包目标仍是 PC，需通过 HTTP/HTTPS 服务加载。尚未上传外部发布平台。

重建：运行 `python tools/release.py`。单独更新惯用 Windows build 目录可运行 `tools/package.ps1`。场景 HUD 的离线增量作者为 tools/author_release.py。
