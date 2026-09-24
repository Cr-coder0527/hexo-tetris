# 俄罗斯方块小游戏 · Hexo Tetris

一个使用**原生 HTML + CSS + JavaScript** 实现的俄罗斯方块小游戏，**零依赖、单文件**，可直接嵌入 Hexo 等静态博客，也可独立部署到 GitHub Pages / Vercel / Netlify。

🎮 **在线试玩**：<https://cr-coder0527.github.io/hexo-tetris/>

## ✨ 功能特性

- 标准 7 种方块（I / O / T / S / Z / J / L）
- 顺时针 / 逆时针旋转，带简单踢墙（Wall Kick）
- 软降（↓）与一键硬降（空格）
- **落点幽灵投影**（Ghost Piece）
- **下一个方块**预览
- 计分系统：消 1 / 2 / 3 / 4 行分别得 100 / 300 / 500 / 800 分（乘以当前等级）
- 每消除 10 行提升 1 级，下落速度逐级加快
- 暂停 / 继续 / 重新开始
- 响应式布局，移动端自动显示触控按钮
- 立体配色方块，绿色主题

## 🕹️ 操作方式

| 按键 | 功能 |
| --- | --- |
| ← / → | 左右移动 |
| ↓ | 加速下落（+1 分/格） |
| ↑ 或 X | 顺时针旋转 |
| Z | 逆时针旋转 |
| 空格 | 直接落底（+2 分/格） |
| P | 暂停 / 继续 |
| R | 重新开始 |

手机端会自动显示屏幕触控按钮。

## 📁 项目结构

```
hexo-tetris/
└── index.html   # 游戏全部代码（结构 + 样式 + 逻辑都在这一个文件）
```

## 🚀 在 Hexo 博客中接入

1. 将 `index.html` 放到博客源码目录：

   ```
   source/games/tetris/index.html
   ```

2. 为了避免 Hexo 向该页面注入主题代码（出现重复标题等问题），在站点根目录的 `_config.yml` 中添加：

   ```yaml
   skip_render:
     - games/tetris/index.html
   ```

3. 在主题导航菜单（以 hexo-theme-matery 为例，主题 `_config.yml`）中添加入口：

   ```yaml
   menu:
     Tetris:
       url: /games/tetris/
       icon: fas fa-gamepad
   ```

4. 执行 `hexo clean && hexo g && hexo s`，访问 `http://localhost:4000/games/tetris/` 即可。

## 📦 独立部署

仓库本身就是静态站点，推送到 GitHub 后在仓库 **Settings → Pages** 中选择 `main` 分支根目录即可，无需任何构建。

## 📄 License

[MIT](./LICENSE)
