## Convert colon emojis in to emoji automatically

Okay this has quite a specific/niche use-case.

Sometime you might find yourself using the colon syntax for emojis in your Jekyll blog, because that's how GitHub, Gitter, Slack, and other places do it. But Jekyll doesn't know how to handle these colon emojis.

So you might type `:boom:` expecting to get the 💥 emoji, but sadly you won't.

With this little Jekyll snippet that I've made, you can define a list of colon emojis and their actual emoji counter parts, and then use the include in place of your regular text. The list of emojis that are available these days is quite exhaustive (I think we're at about 1300?) so I've only included three to demonstrate how this works.

Take a look at [`_includes/emojify.html`](https://github.com/omgmog/jekyll-colon-emoji/blob/master/_includes/emojify.html), the title of [`_posts/2015-10-20-welcome-to-jekyll.markdown`](https://github.com/omgmog/jekyll-colon-emoji/blob/master/_posts/2015-10-20-welcome-to-jekyll.markdown), and the place we output the title in [`index.html`](https://github.com/omgmog/jekyll-colon-emoji/blob/master/index.html#L16)

```
---
title:  "Welcome to Jekyll! :grin: :boom:"
---
```

```
{% include emojify.html text=post.title %}
```

