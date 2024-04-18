---
title: Home
layout: base.njk
tags: navItem
---


## Families
Here is a list of all Families
<section class="grid">
{% for post in collections.family %}
<article class="card">
    <!-- <div class="card__img"><video src="/media/{{ post.data.video | url }}" alt="{{ post.data.postImgAlt}}"></div> -->
    <div class="card__video">
        <video controls width="250">
            <source src="/media/{{ post.data.video}}" type="video/mp4" />
        </video>
    </div>
      <div class="card__content">
        <h1 class="card__header">{{ post.data.title }}</h1>
        <p class="card__text">{{ post.data.description }}</p>
        <a href="{{ post.url }}"> <button class="card__btn">Explore <span>&rarr;</span></button></a>
      </div>
    </article>
    {% endfor %}
</section>
