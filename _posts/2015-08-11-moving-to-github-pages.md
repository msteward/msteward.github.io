---
layout: post
title: Moving to Github Pages
date: '2015-08-11T18:30:00.001-08:00'
author: Michael Steward
comments: true
---

I've recently moved this blog over to [GitHub Pages](https://pages.github.com/) as I was finding Blogger too bloated for what I wanted. I was already very familiar with GitHub so the move was relatively straight forward and thanks to Jekyll and the [import tool for Blogger sites](http://import.jekyllrb.com/docs/blogger/) all content came with the move.

Jekyll is a static website tool. What does this mean? Well for a start forget the back end; Jekyll generates your blog content from Markdown files into pre-formatted, ready to serve HTML files. This means no back end database, no server side scripting; just plain HTML being served straight up. For some this would be too much of a limiting factor but for a simple blog like this it's perfect. 

When moving from Blogger make sure to setup your permalink format to match so that any links out there continue to work for simplicity. For me that meant updating `_config.yml` to:

{% highlight yaml %}
permalink: /:year/:month/:title.html
{% endhighlight %}

Integrating Google Analytics was also straight forward. Jekyll provides a `default.html` layout template which you can add your Analytics snippet to. I keep the code in a separate file inside the `includes` folder and add it to the default layout:

`{% raw %}
  </body>
  {% include google_analytics.html %}
</html>
{% endraw %}`

So far I'm happy with the simplicity. Next step is to setup [Cloudflare](https://www.cloudflare.com) for always on SSL and CDN goodness. 
