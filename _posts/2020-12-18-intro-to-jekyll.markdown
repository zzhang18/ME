---
title: 运用Jekyll自动生成博客
date: 2020-12-18 09:00:32 Z
categories:
- jekyll
tags:
- jekyll
layout: post
---

You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve`, which launches a web server and auto-regenerates your site when a file is updated.

To add new posts, simply add a file in the `_posts` directory that follows the convention `YYYY-MM-DD-name-of-post.ext` and includes the necessary front matter. Take a look at the source for this post to get an idea about how it works.

Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}


Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

## Jekeyll Website setup:

1. Follow [Jekyll docs][jekyll-docs] to create blog website
2. Follow the [Github Page Guide][GitHub Pages site with Jekyll]
3. Upated url and baseUrl in _config.yml 
4. Publish

{% highlight cpp %}
Jekyll new yourProject
cd yourProject  
bundle exec Jekyll serve
{% endhighlight %}
{% highlight yml %}
baseurl: "/ME" # the subpath of your site, e.g. /blog
url: "http://zzhang18.github.io" # the base hostname & protocol for your site, e.g. http://example.com
{% endhighlight %}

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
[GitHub Pages site with Jekyll]:https://docs.github.com/en/free-pro-team@latest/github/working-with-github-pages/setting-up-a-github-pages-site-with-jekyll

## Reference:
- [jekyll-docs](https://jekyllrb.com/docs/home)
- [jekyll-gh](https://github.com/jekyll/jekyll)
- [GitHub Pages site with Jekyll](https://docs.github.com/en/free-pro-team@latest/github/working-with-github-pages/setting-up-a-github-pages-site-with-jekyll)
- [Jekyll - Static Site Generator - Tutorial](https://www.youtube.com/playlist?list=PLLAZ4kZ9dFpOPV5C5Ay0pHaa0RJFhcmcB)
