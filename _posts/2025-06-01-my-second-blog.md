---
layout: single
title: 我的第二篇博客
date: 2025-06-01
categories: [博客, 技术]
tags: [Jekyll, GitHub Pages]
---


大家好！这是我的第二篇博客文章。

<!-- 在[第一篇博客](http://localhost:4000/博客/生活/2025/04/05/my-first-blog.html)中，我分享了如何搭建一个 GitHub Pages 网站。今天，我想聊聊我在学习 Jekyll 过程中发现的一些新功能，以及一些有用的资源。 -->

## 学习 Jekyll 的新功能

最近，我深入研究了 Jekyll 的配置文件 `_config.yml`。通过调整配置，我学会了如何为网站添加更多个性化功能，例如：

- **设置 baseurl**：如果你的网站不是部署在根目录，可以在 `_config.yml` 中设置 `baseurl`，比如 `baseurl: "/my-blog"`。
- **使用插件**：Jekyll 支持插件，比如 `jekyll-seo-tag`，可以自动为页面生成 SEO 元信息，提升搜索引擎可见性。

我还尝试了 Liquid 模板语言的一些高级用法，比如用 `where` 过滤器筛选特定分类的文章：

```liquid
{% assign tech_posts = site.posts | where: "categories", "技术" %}
{% for post in tech_posts %}
- [{{ post.title }}]({{ post.url }})
{% endfor %}
```

## 分享一些资源

在学习过程中，我发现了一些非常有用的资源，推荐给大家：

- [Jekyll 官方文档](https://jekyllrb.com/docs/)：详细介绍了 Jekyll 的所有功能，适合初学者和进阶用户。
- [GitHub Pages 指南](https://docs.github.com/en/pages)：GitHub 官方提供的 Pages 部署教程，包含常见问题解答。
- [Liquid 模板语言参考](https://shopify.github.io/liquid/)：学习 Liquid 语法的绝佳资源，尤其是过滤器和标签的用法。

## 下一步计划

接下来，我计划为我的网站添加一个“关于”页面，介绍更多关于我的信息。同时，我也想尝试使用 Jekyll 的数据文件（`_data` 文件夹）来管理一些静态内容，比如导航菜单。

希望这篇博客对你有帮助！如果你有任何建议，欢迎留言。

<!-- [返回首页](http://localhost:4000/) -->