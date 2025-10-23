# CSA TechHub 官方网站

计算机科学协会技术中心的官方网站。

## 本地开发

### 安装依赖

```bash
bundle install --path=vendor/bundle
npm install
```

### 本地预览

```bash
bundle exec jekyll serve
```

然后访问 <http://localhost:4000/> 预览网站。

### 构建网站

```bash
bundle exec jekyll build
```

生产环境构建：

```bash
JEKYLL_ENV=production bundle exec jekyll build
```

## Markdown 格式化

使用 prettier 进行格式化：

```bash
# 检查格式
npm run check

# 自动格式化
npm run fix
```

## 项目结构

```
csa-techhub/
├── _config.yml          # Jekyll 配置文件
├── _data/              # 数据文件
│   ├── navigation.yml  # 导航配置
│   └── authors.yml     # 作者信息
├── pages/              # 页面和集合
│   ├── _wiki/          # Wiki 文档集合
│   ├── _news/          # 新闻动态集合
│   │   └── 2025/       # 按年份组织
│   ├── _pages/         # 其他静态页面
│   ├── csa-hub.md      # CSA-hub 板块
│   └── ctf.md          # CTF 板块
├── assets/             # 静态资源
│   └── css/           # 样式文件
├── index.md            # 首页
└── Gemfile             # Ruby 依赖
```

## 添加内容

### 添加 Wiki 页面

在 `pages/_wiki/` 目录下创建 Markdown 文件。

### 添加新闻

在 `pages/_news/2025/` (或对应年份) 目录下创建 Markdown 文件。

## 许可

MIT License
