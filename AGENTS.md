# AI Infra 学习社区文档项目

## About this project

- 这是一个 AI Infra 学习社区网站，基于 [Mintlify](https://mintlify.com) 构建
- 网站包含三大板块：**在线分享**、**读书会**、**学习资源**
- 页面使用 MDX 格式，带 YAML frontmatter
- 配置文件为 `docs.json`
- 运行 `mint dev` 本地预览
- 运行 `mint broken-links` 检查链接

## Site structure

- `index.mdx` — 社区首页
- `about.mdx` — 关于社区
- `how-to-join.mdx` — 如何参与
- `talks/` — 在线分享
  - `index.mdx` — 分享概览
  - `01-vllm-quickstart.mdx` — 各期分享页面
- `books/<book-slug>/` — 读书会，每本书一个目录
  - `index.mdx` — 书籍概览
  - `schedule.mdx` — 阅读计划
  - `chapters/ch01.mdx` — 各章节笔记
  - `resources.mdx` — 延伸资源
- `resources/` — 学习资源
  - `index.mdx` — 资料概览
  - `llm-inference.mdx` — 按主题分类的资料页面

## Adding a new talk

1. 在 `talks/` 下创建新的 MDX 文件，如 `talks/08-new-topic.mdx`
2. 在 `docs.json` 的 `navigation.tabs` → "在线分享" tab 中添加页面路径
3. 更新 `talks/index.mdx` 的卡片列表

## Adding a new book

1. 在 `books/` 下创建新目录，如 `books/new-book/`
2. 创建 `index.mdx`、`schedule.mdx`、`resources.mdx` 和 `chapters/` 目录
3. 在 `docs.json` 的 `navigation.tabs` → "读书会" tab 的 `dropdowns` 数组中添加新的 dropdown 项

## Adding a new resource topic

1. 在 `resources/` 下创建新的 MDX 文件，如 `resources/new-topic.mdx`
2. 在 `docs.json` 的 `navigation.tabs` → "学习资源" tab 中添加页面路径
3. 更新 `resources/index.mdx` 的卡片列表

## Style preferences

- 中文内容为主
- Use active voice
- Second person can appear in prose when natural, but avoid teaching-style phrasing such as “你要”“你该”“先记住”
- Keep sentences concise
- Prefer a public technical article / blog tone over lecture notes or guided-reading tone
- Use direct, content-first headings
- Prefer noun phrases or direct declarative headings over question-style headings
- Avoid headings or table labels built around “为什么”“这一章”“这里”“下面”“先理解”“记住”“你要”“你该”
- Avoid meta-commentary about chapter structure; focus on the subject itself rather than “this chapter wants to say...”
- Avoid rhetorical “why” sentences in body copy; state the conclusion directly
- When adding internet-sourced material, add direct hyperlinks at first mention or in key tables, not only in a final reading list
- Code formatting for file names, commands, paths
