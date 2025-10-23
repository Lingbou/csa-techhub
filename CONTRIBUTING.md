# 贡献指南

感谢你对 CSA TechHub 网站的贡献！

## 如何贡献

### 报告问题

如果你发现了 bug 或有功能建议：

1. 在 GitHub Issues 中搜索是否已有类似问题
2. 如果没有，创建新 Issue
3. 清晰描述问题或建议

### 提交代码

1. Fork 本仓库
2. 创建你的特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交你的更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 创建 Pull Request

## 代码规范

### Markdown 文件

- 使用 Prettier 格式化所有 Markdown 文件
- 运行 `npm run fix` 自动格式化
- 提交前运行 `npm run check` 确保格式正确

### Front Matter 规范

每个页面都应该包含适当的 front matter：

```yaml
---
title: '页面标题'
permalink: /path/to/page/
layout: single
toc: true # 如果需要目录
---
```

### 提交信息规范

使用清晰的提交信息：

- `feat: 添加新功能`
- `fix: 修复 bug`
- `docs: 更新文档`
- `style: 格式调整`
- `refactor: 代码重构`
- `test: 添加测试`
- `chore: 构建/工具相关`

## Pull Request 流程

1. 确保代码通过所有检查（Prettier、构建等）
2. 更新相关文档
3. 在 PR 描述中详细说明更改内容
4. 等待审核和反馈
5. 根据反馈进行调整

## 内容贡献

### 添加 Wiki 文档

1. 参考 `_wiki/_template.md` 创建新文档
2. 确保内容准确、清晰
3. 添加适当的代码示例和图片
4. 更新 `_data/navigation.yml` 添加导航链接

### 添加新闻动态

1. 参考 `_news/_template.md` 创建新文章
2. 使用正确的日期格式命名文件
3. 设置 author 字段

## 本地测试

提交前请确保：

```bash
# 格式检查通过
npm run check

# 网站可以正常构建
bundle exec jekyll build

# 本地预览正常
bundle exec jekyll serve
```

## 需要帮助？

- 查看 [QUICKSTART.md](QUICKSTART.md)
- 在 Issues 中提问
- 联系维护者

感谢你的贡献！🎉
