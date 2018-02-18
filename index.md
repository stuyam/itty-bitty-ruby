---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: default
---

<div class="container mx-auto px-4 max-w-xl">
  <div class="flex">
  {% for post in site.posts %}
    <div class="w-1/2 p-8">
      <a href="{{ post.url }}" class="post-card bg-white mx-auto max-w-sm shadow-lg rounded-lg overflow-hidden px-6 py-4 block no-underline text-black">
        <h3 class="text-center text-xl font-normal mb-1">{{ post.title }}</h3>
        <h6 class="text-center text-base text-grey-dark font-normal mb-3">{{ post.date | date_to_string }}</h6>
        <img class="w-100" src="{{ site.url }}/img/comics/{{ post.title | slugify }}.png" />
        <div class="flex justify-center items-center mt-4">
          <span href="#" class="bg-red text-white rounded-full text-sm py-1 px-2 mr-3">Unread</span>
          <span class="text-lg text-grey-dark mr-3">View Code</span>
          <img class="w-8 h-8" src="{{ site.url }}/img/disclosure-indicator.png" />
        </div>
      </a>
    </div>
  {% endfor %}
</div>
