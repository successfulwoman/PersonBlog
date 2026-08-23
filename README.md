# CC 和 LL 的个人博客

> 一个开放的娱乐平台 —— 记录生活，分享知识与有趣内容

这是 **CC 和 LL** 的个人博客。博客基于 [astro-koharu](https://github.com/cosZone/astro-koharu) 主题定制搭建，采用二次元萌系粉蓝风格。这里会分享我们的日常生活、学习笔记、好用工具以及各种娱乐内容。

## ✨ 功能特性

- **萌系 / 二次元 / 粉蓝配色**，支持深色模式，站标为定制的 `LL&CC` 矢量 Logo
- **Markdown 增强**：代码高亮、数学公式（KaTeX）、流程图（Mermaid）、交互测验（Quiz）、链接卡片预览、Shoka 语法等
- **内容组织**：多级分类、标签、文章归档，支持草稿与置顶
- **Pagefind 无后端全站搜索**，纯静态即可搜索
- **LQIP 占位图**：图片加载前显示渐变色占位，体验更顺滑
- **多语言界面**：中文 / 英文 / 日文，支持 RSS 订阅
- **自定义站点图标与头像**、文章加密访问
- **可选功能**（默认关闭，按需在配置中开启）：评论区、访问统计、背景音乐、追番页面、圣诞特效、碎碎念动态

## 🛠 技术栈

[Astro](https://astro.build/) 7 · [React](https://react.dev/) 19 · [Tailwind CSS](https://tailwindcss.com/) 4 · TypeScript · Pagefind

## 🚀 快速开始

```bash
# 安装依赖
pnpm install

# 本地开发（http://localhost:4321）
pnpm dev

# 生产构建（输出到 dist/）
pnpm build

# 本地预览构建产物
pnpm preview
```

## ✍️ 发布文章

1. 在 `src/content/blog/` 对应分类目录下新建 Markdown 文件（可复制根目录的 `_template.md` 模板）
2. 填写 frontmatter：标题、日期、分类、标签等
3. 保存后 `pnpm dev` 本地预览，确认无误后构建部署

📄 详细的字段说明和发布流程见仓库内的 **《发布帖子使用说明.docx》**。

也支持交互式创建：

```bash
pnpm koharu new post   # 向导式新建文章
```

## 📁 项目结构

```plain
src/
├── content/blog/   # 博客文章（Markdown，按分类分子目录）
├── components/     # UI 组件
├── pages/          # 路由页面
├── i18n/           # 多语言翻译
└── lib/            # 工具函数
config/site.yaml    # 站点配置（标题、分类、导航、功能开关）
public/             # 静态资源（图片、字体、图标）
docker/             # Docker 部署配置
cms/                # 本地可视化 CMS
```

## 📦 部署

项目默认输出纯静态站点，可部署到任意静态托管（Nginx、Vercel、Netlify 等），也支持 Docker 一键部署：

```bash
# 1. 创建环境配置（可自定义端口）
cp .env.example .env

# 2. 构建并启动（Nginx 容器）
docker compose --env-file ./.env -f docker/docker-compose.yml up -d --build
```

## ⚙️ 站点配置

所有站点信息都集中在 `config/site.yaml` 一个文件里：网站标题与副标题、头像、分类映射、导航菜单、社交链接、功能开关等。修改后重新构建即可生效。

## 🙏 致谢

本博客基于 [astro-koharu](https://github.com/cosZone/astro-koharu) 主题定制，设计灵感来自 Hexo 的 [Shoka](https://shoka.lostyu.me/) 主题，感谢原作者们的开源贡献。
