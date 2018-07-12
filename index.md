---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: default
---

<div class="container mx-auto max-w-xl">
  <div class="flex flex-wrap">
  {% for post in site.posts limit:4%}
    {% include post-card.html post=post %}
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
  {% for post in site.posts offset:4%}
    {% include post-card.html post=post %}
  {% endfor %}
</div>
