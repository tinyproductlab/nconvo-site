# netchat-site

NConvo（内部代号 NetChat）的产品官网，**纯静态单文件 HTML，无构建步骤**。

线上地址（GitHub Pages）：https://nconvo.tinylabpro.com/

## 文件说明

- `index.html` — 主页，所有 CSS/文案（中英双语）都在这一个文件里
- `privacy.html` / `terms.html` / `about.html` — 短政策页，样式内联
- `robots.txt` / `sitemap.xml` — SEO 收录配置
- `favicon.ico`、`favicon-16x16.png`、`favicon-32x32.png`、`apple-touch-icon.png` — 站点图标（根目录）
- `assets/` — 品牌图标、截图、赞赏码

## 如何改内容

- **改文字**：直接编辑 `index.html`。带 `data-zh` / `data-en` 属性的元素支持右上角中英切换，两个语言都要改。
- **加长文 / FAQ**：`index.html` 底部 `<script>` 里的 `ARTICLE_ZH` / `ARTICLE_EN` 两个模板，按语言整段渲染；头部 JSON-LD 里的 FAQPage 记得同步。
- **换截图**：把新图放进 `assets/`，然后改脚本里的 `HERO_SHOTS`（顶部轮播，竖屏最佳）和 `ALL_SHOTS`（界面预览网格），提交即可。
- **调主题色**：`index.html` CSS `:root` 里的 `--primary` / `--accent` 等变量。

## 部署

GitHub Pages 已开启：**main 分支 / 根目录**。推送到 main 后 1~2 分钟自动发布，无需其他操作。
