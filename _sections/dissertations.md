---
title: Dissertations
layout: page
date: 04/01/1100
---

<div>
<div class="band">
  {% for post in site.dissertations %}
    <a href="{{ post.link }} " class="card">
      <img class="card-img-top" src="../../assets/{{ post.image }}" alt="Card image cap">
      <div class="card-body">
      <div class="container">
        <h5 class="card-title">{{ post.title }}</h5>
        <!-- <p class="card-text">{{  post.blurb  }} </p> -->
        <p class="card-author-list">{{ post.keywords }}</p>

      </div>
    </div>
    </a>
  {% endfor %}
</div>
<h2>
