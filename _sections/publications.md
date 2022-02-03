---
title: Publications
---

<div>
<h2>
As a First Author:
</h2>
<div class="band">
  {% for post in site.bibfirst %}
    <a href="{{ post.link }} " class="card">
      <img class="card-img-top" src="../../assets/{{ post.image }}" alt="Card image cap">
      <div class="card-body">
      <div class="container">
        <h5 class="card-title">{{ post.title }}</h5>
        <!-- <p class="card-text">{{  post.blurb  }} </p> -->
        <p class="card-author-list">{{ post.authors }}</p>
        <p class="card-venue">{{ post.venue }}</p>
      </div>
    </div>
    </a>
  {% endfor %}
</div>
<h2>
As an Et Al:
</h2>
<div class="band">
  {% for post in site.bibetal %}
    <a href="{{ post.link }} " class="card">
      <!-- <img class="card-img-top" src="../../assets/{{ post.image }}" alt="Card image cap"> -->
      <div class="card-body">
      <div class="container">
        <h5 class="card-title">{{ post.title }}</h5>
        <!-- <p class="card-text">{{  post.blurb  }} </p> -->
        <p class="card-author-list">{{ post.authors }}</p>
        <p class="card-venue">{{ post.venue }}</p>
      </div>
    </div>
    </a>
  {% endfor %}
</div>
</div>