# 夏之博客数据仓库

夏之博客（520pro.top）的文章数据源，Markdown 源文件 + 构建脚本。

## 结构

- `posts/*.md` —— 文章 Markdown 源（frontmatter + 正文）
- `img/` —— 正文图片
- `generate-posts.js` —— 生成 `posts.json` / 分页 / `rss.xml` / SEO 静态页
- `convert-to-webp.js` —— 旧格式图片批量转 WebP

## 输出与部署

构建产物写入 `dist/`，由 Cloudflare Workers（raw-posts.520pro.top）托管。

```bash
npm install
node convert-to-webp.js
node generate-posts.js
```

## 许可证

[MIT](LICENSE)