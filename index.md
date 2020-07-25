---
layout: default
title: My Blog
---

<h1>Intro</h1>
<p>I've been into Cloud journey for a quite sometime now.This led me to create my own list of notes. Opinions are my own.</p>

<div id="home">
  <h1>Blog Posts</h1>
  <ul class="posts">
    {% for post in site.posts %}
      <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>

  </div>