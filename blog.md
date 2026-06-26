---
layout: default
title: 博客 - 谷歌加速器
description: 谷歌加速器官方博客 - 产品更新、使用教程、网络加速技巧，助您畅享全球网络。
permalink: /blog/
---

<section class="blog-index">
  <div class="container">
    <h1 class="page-title">博客</h1>
    <p class="page-description">产品更新、使用教程、网络加速技巧，助您畅享全球网络。</p>

    <div class="posts-list">
      {% for post in site.posts %}
      <article class="post-card">
        <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
        <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%Y年%m月%d日" }}</time>
        <p>{{ post.excerpt | strip_html | truncate: 180 }}</p>
        <a href="{{ post.url | relative_url }}" class="read-more">阅读全文 →</a>
      </article>
      {% endfor %}
    </div>

    {% if site.posts.size == 0 %}
    <div class="no-posts">
      <p>暂无文章，敬请期待。</p>
    </div>
    {% endif %}
  </div>
</section>
