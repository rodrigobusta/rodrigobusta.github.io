---
permalink: /
layout:    default
title:     Home
---

<!-- {% capture location %}{{ page.url | remove_first:'/' | split:'/' | first }}{% endcapture %}
<nav><ul>
	<li><a {% if location == 'about' %}class="active" {% endif %}href="/about/">About</a></li>
	<li><a {% if location == 'projects' %}class="active" {% endif %}href="/projects/">Projects</a></li>
	<li><a {% if location == 'blog' %}class="active" {% endif %}href="/blog/">Blog</a></li>
	<li><a {% if location == 'contact' %}class="active" {% endif %}href="/contact/">Contact</a></li>
</ul></nav>
 -->
<div class="home">

  <h1 class="page-heading">Últimas postagens</h1>

  <ul class="post-list">
    {% for post in site.posts %}
      <li>
        <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>

        <h2>
          <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
        </h2>
      </li>
    {% endfor %}
  </ul>

  <p class="rss-subscribe">Inscrever-se <a href="{{ "/feed.xml" | prepend: site.baseurl }}">via RSS</a></p>

</div>
