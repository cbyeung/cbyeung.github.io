---
layout: post
title:  My first foray into Jekyll & Github Pages
date:   2017-05-11
categories: jekyll tutorials github
tags: jekyll tutorials github
---
I can find this post in my `_posts` directory. I can rebuild the site in many different ways, but the most common way is to run `jekyll serve`, which launches a web server at `localhost:4000` and auto-regenerates my site when any file (except `_config.yml`) is updated.

To add new posts, simply add a file in the `_posts` directory that follows the convention `YYYY-MM-DD-name-of-post.ext` and includes the necessary front matter. Take a look at the source for this post to get an idea about how it works.

Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def show
  @widget = Widget(params[:id])
  respond_to do |format|
    format.html # show.html.erb
    format.json { render json: @widget }
  end
end
#=> some Ruby code from Jekyll
{% endhighlight %}

{% highlight python %}
def add(m,n):
  p = m + n
  return p
# some silly python code
{% endhighlight %}

Picture of a pretty HondaJet:

![HondaJet]({{ site.url }}/images/hondajet.jpg){:.full-width}

Do tables work?

| time | squared | capacity |
| --- | --- | --- |
| 0 | 0 | yes |
| 1 | 1 | yes |
| 2 | 4 | no |
| 3 | 9 | no |
| 4 | 16 | maybe |
{:.table}
<br><!--This is a forced line break; note that HTML tags easily integrate into markdown-->
No, unfortunately not as is. Update: after adding a `.table` style to `_base.scss`, it now works perfectly. Note: in the command line, locate gems with `bundle show [gem_name]`.

Some `MathJax`? Try this on for size: $$x^2$$. Or this?

\\[\sin{\theta} = \frac{e^{ix}-e^{-ix}}{2i}.\\]

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
