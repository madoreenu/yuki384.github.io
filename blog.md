---
layout: default
title: BLOG
---
<div class="post-head">
{% include header.html %}
<h2>{{page.title}}</h2>
</div>
<div class="gray">
  <section class="Blog">
    {% for post in site.data.blog %}
    <a href="{{ post.url }}" class="post">
    <article>
      {% if post.img %}
      <img src="{{post.img}}" alt="" class="blog-thumbnail" loading="lazy">
      {% else %}
      <img src="/img/thumbnail.jpg" alt="" class="blog-thumbnail" loading="lazy">
      {% endif %}
      <div class="post-text">
        <p>{{post.date | date:"%Y/%m/%d"}}</p><h3>{{post.title}}</h3>
      </div>
    </article>
    </a>
    {% endfor %}
  </section>
</div>
