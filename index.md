---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: default
---

<div class="container mx-auto max-w-xl">
  <div class="flex flex-wrap">
  {% for post in site.posts limit:2%}
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
  <div class="w-full">
    <!-- Mailchimp Subscribe Form -->
    <div class="max-w-sm w-100 mx-auto">
      <form action="https://ittybittyruby.us17.list-manage.com/subscribe/post?u=80abdb57d023e49f8cb8ba09d&amp;id=7df66977b1" method="post" id="mc-embedded-subscribe-form" name="mc-embedded-subscribe-form" class="validate" target="_blank" novalidate>
        <!-- real people should not fill this in and expect good things - do not remove this or risk form bot signups-->
        <div style="position: absolute; left: -5000px;" aria-hidden="true"><input type="text" name="b_80abdb57d023e49f8cb8ba09d_7df66977b1" tabindex="-1" value=""></div>
        <label for="mce-EMAIL" class="block text-grey-darker text-sm font-bold mb-2 text-center">Want more? Subscribe to our mailing list.</label>
        <div class="flex justify-center">
          <input type="email" value="" name="EMAIL" class="email shadow appearance-none border rounded py-2 px-3 text-grey-darker mr-2 w-64" id="mce-EMAIL" placeholder="Email" required>
          <input type="submit" value="Subscribe" name="subscribe" id="mc-embedded-subscribe" class="button bg-red hover:bg-red-light text-white font-bold py-2 px-4 border-b-4 border-red-dark hover:border-red rounded cursor-pointer">
        </div>
      </form>
    </div>
  </div>
  {% for post in site.posts offset:2%}
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
