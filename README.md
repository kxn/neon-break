# 霓虹破碎 / NEON BREAK

赛博朋克街机清版动作 Demo，Godot 4.7.2，支持 PC 键盘与手柄。

**[在线试玩](https://blog.kangkang.org/neon-break/)** · **[Windows 下载](https://github.com/kxn/neon-break/releases/latest)**

Windows 版：在 Release 页下载 `NeonBreak-v18-windows.zip`，完整解压后运行 `NeonBreak.exe`，保持 PCK 与 EXE 同目录，无需安装 Godot。附件同时提供 SHA-256 校验文件。

点击游戏画面开始。WASD / 方向键移动，J 攻击，K / 空格跳跃，E 拾取或丢弃武器，Shift 冲刺，Esc 暂停。完整操作见 [PLAY.md](PLAY.md)。建议使用新版 Chrome、Edge 或 Firefox。

仓库文件保存 Web 发布产物，Windows 压缩包放在 Releases。推送 main 后 GitHub Pages 自动更新，博客的 Hugo 仓库与构建流程保持独立。

游戏通过 Godot PWA Service Worker 提供多线程所需的跨源隔离，首次访问可能自动刷新。请使用 HTTPS，并保持所有导出文件在同一目录。Service Worker 的作用域是 /neon-break/，不接管博客根目录。

本地预览：安装 Python 3，在此目录运行 python serve.py，打开 http://localhost:8068/ 。不能通过双击 index.html 启动。

第三方授权见 [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md)。
