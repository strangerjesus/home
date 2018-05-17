---
layout: default
title: Home
---

<ul class="post-list">
    {% for post in site.posts %}
      <li>
<article class="post-article">
  <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
 {% if post.img !=null %}
          <figure>
              <img src="/img/posts/{{ post.img }}" class="post-img" alt="{{ post.caption }}">
            </a>
              <figcaption>{{ post.caption }}</figcaption>
          </figure>
  {% endif %}

  <div class="content">
      {{ post.content }}
  </div>
  <div>
    <span class="post-meta">{{ post.date | date: "%B %-d, %Y" }}</span>
  </div>
</article>
  </li>
    {% endfor %}
  </ul>


