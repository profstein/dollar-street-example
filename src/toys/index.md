---
title: Most Loved Toys
layout: base.njk
tags: navItem
---


## Most Loved Toys
Here is a list of all Families
<section class="grid">
{%- for post in collections.toy %}
<article class="card">
    <div class="card__media">
        {%- if post.data.image %}
        <img src="/media/{{post.data.image}}" alt="{{ post.data.imageAlt}}">
        {%- elif post.data.video %}
        <video controls width="250">
            <source src="/media/{{post.data.video}}" type="video/mp4" />
        </video>
        {%- endif %}
    </div>
      <div class="card__content">
        <h1 class="card__header">{{ post.data.title }}</h1>
        <p class="card__text">{{ post.data.description }}</p>
        <a href="{{ post.url }}"> <button class="card__btn">Explore <span>&rarr;</span></button></a>
      </div>
    </article>
{%- endfor %}
</section>