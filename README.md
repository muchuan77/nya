# muchuan's home（Hexo 博客）

基于 [Hexo](https://hexo.io/) 的静态个人博客站点源码，用于写作、归档与部署。

## 站点信息

| 项 | 说明 |
| --- | --- |
| 站点标题 | muchuan's home |
| 副标题 | Welcome to the moon |
| 作者 | Muchuan |
| 语言 / 时区 | `zh-CN` / `Asia/Shanghai` |
| 永久链接 | `:year/:month/:day/:title/` |

具体文案与 SEO 相关项可在根目录 `_config.yml` 中修改；上线前请将 `url` 改为实际域名（当前示例为 `http://example.com`）。

## 技术栈

- **Hexo** 7.x
- **渲染**：EJS、Marked（Markdown）、Stylus
- **生成器**：首页、归档、分类、标签
- **主题**：在 `_config.yml` 的 `theme` 中配置为 `particlex`（若本地缺少该主题目录，需自行安装对应主题或改为已安装主题，例如依赖中的 `hexo-theme-landscape`）

## 目录结构（简要）

```
nya/
├── _config.yml          # 站点与 Hexo 主配置
├── package.json         # 脚本与依赖
├── scaffolds/           # 新建文章/页面/草稿的模板
├── source/              # 源内容（文章、页面、静态资源）
│   ├── _posts/          # 博文（Markdown）
│   ├── about/           # 关于页等独立页面
│   ├── categories/
│   └── tags/
└── themes/              # 主题（若已安装，通常在此；可能被 .gitignore 忽略）
```

## 本地开发

需要 [Node.js](https://nodejs.org/)（建议 LTS）。

```bash
npm install
npm run server
```

浏览器访问终端提示的本地地址（一般为 `http://localhost:4000`）即可预览。

## 构建与部署

```bash
npm run build    # 生成静态文件到 public/
npm run clean    # 清理缓存与生成目录
npm run deploy   # 一键部署（需在 _config.yml 中配置 deploy）
```

`deploy` 的类型与仓库地址同样在 `_config.yml` 的 `deploy` 段配置；未配置时不会执行实际发布。

## 新建文章

```bash
npx hexo new "文章标题"
```

或在 `source/_posts/` 下按 `scaffolds/post.md` 的 front-matter 格式自行添加 `.md` 文件。

## 其他说明

- 草稿可使用 `scaffolds/draft.md`，默认 `_config.yml` 中 `render_drafts: false`，本地预览草稿需按需开启或使用 Hexo 草稿相关命令。
- 项目含 [Dependabot](https://docs.github.com/en/code-security/dependabot) 配置（`.github/dependabot.yml`），便于依赖更新提醒。

---

个人主页与社交链接见站内 [关于](source/about/index.md) 页面。
