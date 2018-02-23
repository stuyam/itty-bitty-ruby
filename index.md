---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: default
---

<div class="container mx-auto px-4 max-w-xl">
  <div class="flex flex-wrap">
  {% for post in site.posts %}
    <div class="w-full md:w-1/2 p-4 sm:p-8">
      <div class="relative w-full">
        <a href="{{ post.url }}" class="post-card bg-white max-w-sm shadow-lg rounded-lg overflow-hidden px-6 py-4 block no-underline text-black mx-auto">
          <h3 class="text-center text-xl font-normal mb-1">{{ post.title }}</h3>
          <h6 class="text-center text-base text-grey-dark font-normal mb-3">{{ post.date | date_to_string }}</h6>
          <img class="w-100" src="{{ site.url }}/img/comics/{{ post.title | slugify }}.png" />
          <div class="flex justify-center items-center mt-4">
            <span class="text-lg text-grey-dark mr-3">View Code</span>
            <img class="w-8 h-8" src="{{ site.url }}/img/disclosure-indicator.png" />
          </div>
        </a>
        <a href="{{ post.url }}" class="badge text-red rounded-full py-1 px-2 mr-3 leading-none no-underline font-bold"><span class="text-xl">&bullet;</span> Unread</a>
      </div>
    </div>
  {% endfor %}
</div>
