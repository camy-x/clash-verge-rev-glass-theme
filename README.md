# Clash Verge Rev Glass Theme

一套为 Clash Verge Rev 制作的透明磨砂玻璃 CSS 主题，内置背景壁纸。

> 本主题按 **Clash Verge Rev v2.5.2** 制作和测试，**深色主题下效果最佳**。不建议在浅色主题下使用。

## 效果预览

![设置页](docs/preview-settings.png)

![代理页](docs/preview-proxies.png)

## 安装

1. 打开 Clash Verge Rev，进入“设置 → Verge 基础设置 → 主题设置 → CSS 注入”。
2. 将“主题模式”切换为“深色”。
3. 打开 CSS 注入编辑器，按 `Ctrl+A` 全选并删除旧内容，再粘贴 [`injection.css`](injection.css) 的全部内容。
4. 保存 CSS 编辑器，再保存主题设置。
5. 如果界面没有立即刷新，重启 Clash Verge Rev。

## 推荐颜色

```text
主色: #5AB0F8
次色: #F58BA6
主文字色: #FFFFFF
次文字色: #EBEBF599
信息色: #7FC8FF
警告色: #F5B45C
错误色: #FF6B80
成功色: #3FD3A8
```

![主题颜色设置](docs/theme-colors.png)

## 更换背景图

默认背景图位于 [`assets/wallpaper.jpg`](assets/wallpaper.jpg)，CSS 会通过 GitHub Raw 地址自动加载。

此方式需要能够访问 GitHub Raw。图片暂时加载失败时，主题会安全回退为深色背景，不会出现白屏。

如果你维护自己的 Fork，推荐用新图片替换 `assets/wallpaper.jpg`，并在 `injection.css` 顶部把 `--cv-wallpaper` 中的用户名、仓库名和分支名改成自己的实际地址。仓库必须公开，Raw 图片才能直接加载。

也可以直接改成其他图片直链：

```css
--cv-wallpaper: url("https://example.com/wallpaper.jpg");
```

背景太亮或太暗时，调整 `injection.css` 顶部的遮罩透明度：

```css
--cv-scrim: rgba(6, 8, 14, 0.50);
```

最后一个数值越大，背景越暗；越小，背景越亮。

## 兼容性

- 已针对 Clash Verge Rev v2.5.2 深色模式检查。
- 主题依赖当前版本的页面结构和 Chromium `:has()` 选择器。
- Clash Verge Rev 升级后若页面结构变化，个别组件可能需要重新适配。
- 本项目不是 Clash Verge Rev 官方主题。

## 许可证

CSS 与文档使用 [MIT License](LICENSE)。壁纸来源为“哲风壁纸”，已确认允许公开转载；壁纸不包含在 MIT 许可证内，其他使用方式仍按原作者或来源的授权执行。
