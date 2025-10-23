# 快速开始指南

## 本地开发环境搭建

### 1. 安装依赖

首次使用需要安装依赖：

```bash
# 安装 Ruby 依赖
bundle install --path=vendor/bundle

# 安装 Node.js 依赖（用于代码格式化）
npm install
```

### 2. 启动开发服务器

```bash
bundle exec jekyll serve --host 0.0.0.0
```

网站将在 <http://localhost:4000/> 运行。

### 3. 构建网站

```bash
# 开发环境构建
bundle exec jekyll build

# 生产环境构建
JEKYLL_ENV=production bundle exec jekyll build
```

构建结果在 `_site/` 目录。

## 网站结构说明

```
csa-techhub/
├── _config.yml          # Jekyll 主配置文件
├── _data/              # 数据文件
│   ├── navigation.yml  # 导航菜单配置
│   └── authors.yml     # 作者信息
├── pages/              # 所有页面内容
│   ├── _wiki/          # Wiki 文档集合
│   │   └── _template.md    # Wiki 页面模板
│   ├── _news/          # 新闻动态集合
│   │   ├── 2025/       # 2025年新闻
│   │   └── _template.md    # 新闻文章模板
│   ├── _pages/         # 其他静态页面
│   │   ├── about.md    # 关于我们
│   │   ├── join.md     # 加入我们
│   │   ├── wiki.md     # Wiki 首页
│   │   └── news.md     # 新闻首页
│   ├── csa-hub.md      # CSA-hub 板块
│   └── ctf.md          # CTF 板块
├── assets/             # 静态资源
│   └── css/           # 样式文件
└── index.md            # 网站首页
```

## 添加内容

### 添加 Wiki 文档

1. 复制 `pages/_wiki/_template.md`
2. 修改文件名和内容
3. 更新 front matter（标题、链接等）

示例：

```markdown
---
title: 'Docker 入门指南'
permalink: /wiki/docker-guide/
toc: true
---

# Docker 入门指南

内容...
```

### 添加新闻动态

1. 复制 `pages/_news/_template.md`
2. 在对应年份目录下（如 `pages/_news/2025/`）创建文件
3. 按照 `YYYY-MM-DD-title.md` 格式命名
4. 更新 front matter

示例：

```markdown
---
title: 'CSA TechHub 正式成立'
date: 2025-10-23
author: csa_team
---

新闻内容...
```

### 修改导航菜单

编辑 `_data/navigation.yml`：

```yaml
main:
  - title: '首页'
    url: /
  - title: '新菜单项'
    url: /new-page/
```

### 添加作者信息

编辑 `_data/authors.yml`：

```yaml
your_id:
  name: '你的名字'
  bio: '简介'
  avatar: '/assets/images/your-avatar.png'
  links:
    - label: 'GitHub'
      icon: 'fab fa-fw fa-github'
      url: 'https://github.com/yourusername'
```

## 代码格式化

使用 Prettier 保持代码风格统一：

```bash
# 检查格式
npm run check

# 自动格式化
npm run fix
```

## 部署

### GitHub Pages 部署

1. 在 GitHub 仓库设置中启用 Pages
2. 选择 GitHub Actions 作为部署源
3. 推送代码到 main 分支即可自动部署

### 手动部署

```bash
# 构建网站
JEKYLL_ENV=production bundle exec jekyll build

# 将 _site/ 目录内容部署到服务器
```

## 常见问题

### Q: 如何修改网站主题颜色？

编辑 `_config.yml`，修改 `minimal_mistakes_skin` 选项。可选值：

- default
- air
- aqua
- contrast
- dark
- dirt
- neon
- mint
- plum
- sunrise

### Q: 如何添加自定义样式？

在 `assets/css/main.scss` 中添加自定义 CSS。

### Q: 如何配置评论系统？

在 `_config.yml` 中配置评论提供商（如 Disqus、Utterances 等）。

## 参考资源

- [Jekyll 官方文档](https://jekyllrb.com/docs/)
- [Minimal Mistakes 主题文档](https://mmistakes.github.io/minimal-mistakes/)
- [Markdown 语法指南](https://www.markdownguide.org/)
