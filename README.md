# 霓虹破碎 v18 · Web 发布包

面向 PC 浏览器，建议使用当前版 Chrome、Edge 或 Firefox。键盘与手柄操作见 PLAY.md。点击游戏画面后开始，浏览器会在首次交互后开放声音；手柄需先按一个按钮激活。

## 本地试玩

解压到任意文件夹，在该目录运行 `python serve.py`，然后访问 http://localhost:8068/ 。需要 Python 3，Ctrl+C 停止服务器。不要直接双击 index.html；游戏资源需要通过 HTTP 服务加载。

## 网站部署

将目录中全部文件放在同一站点目录，通过 HTTPS 访问 index.html。不要改动导出文件名。WebAssembly 文件的 MIME 类型应为 `application/wasm`。

本包使用多线程及 Stream 音频，保留限幅混音、慢动作变调和摩托引擎变化。服务器建议配置以下响应头：

```
Cross-Origin-Opener-Policy: same-origin
Cross-Origin-Embedder-Policy: require-corp
```

附带 `_headers` 供支持该格式的静态托管平台使用。Godot PWA 的跨源隔离兼容处理也已启用，但目标平台仍需允许 Service Worker；第三方 iframe 还需允许跨源隔离。内嵌游戏平台部署后应再验证音频和手柄。HTTP 公网地址不适合作为最终部署地址。

本地存档/键位存储属于当前浏览器和站点，与 Windows 版不互通。隐私模式或清除站点数据可能清除设置。此包没有触屏操作界面，目标设备仍是 PC。

导出与部署依据：[Godot 4.7 Web 导出文档](https://docs.godotengine.org/en/4.7/tutorials/export/exporting_for_web.html)。
