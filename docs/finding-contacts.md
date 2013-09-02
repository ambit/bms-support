---
layout: docs
title: Finding Contacts
prev_section: filters-and-pagination
next_section: updating-contact-information
permalink: /docs/posts/
---

There are many ways to get to a contact – after all, contacts are at the centre of everything in BMS CRM. A contact is any business or person that is recorded in the CRM database.

In this section, we'll go through a couple of the most common ways of navigating to a specific contact.

By clicking on the contacts icon in the navigation menu, the contacts submenu will appear. From here you can choose to search for a contact, add a new contact, or view the contact list.

## The Contact List

The contact list is a list of all the contacts in the system. By clicking on an item in the index you will be directed to the details page for that contact.

As this list can be very large, you will probably want to use the filter to narrow it down a bit. See [Filters and Pagination](../filters-and-pagination/) for more information.

The contacts submenu includes shortcuts to the full contact list, as well as a number of saved filters.

### Creating Post Files

To create a new post, all you need to do is create a new file in the `_posts`
directory. How you name files in this folder is important. Jekyll requires blog
post files to be named according to the following format:

{% highlight bash %}
YEAR-MONTH-DAY-title.MARKUP
{% endhighlight %}

Where `YEAR` is a four-digit number, `MONTH` and `DAY` are both two-digit
numbers, and `MARKUP` is the file extension representing the format used in the
file. For example, the following are examples of valid post filenames:

{% highlight bash %}
2011-12-31-new-years-eve-is-awesome.md
2012-09-12-how-to-write-a-blog.textile
{% endhighlight %}

### Content Formats

All blog post files must begin with [YAML front- matter](../frontmatter/). After
that, it's simply a matter of deciding which format you prefer. Jekyll supports
two popular content markup formats:
[Markdown](http://daringfireball.net/projects/markdown/) and
[Textile](http://textile.sitemonks.com/). These formats each have their own way
of marking up different types of content within a post, so you should
familiarize yourself with these formats and decide which one best suits your
needs.

## Including images and resources

Chances are, at some point, you'll want to include images, downloads, or other
digital assets along with your text content. While the syntax for linking to
these resources differs between Markdown and Textile, the problem of working out
where to store these files in your site is something everyone will face.

Because of Jekyll’s flexibility, there are many solutions to how to do this. One
common solution is to create a folder in the root of the project directory
called something like `assets` or `downloads`, into which any images, downloads
or other resources are placed. Then, from within any post, they can be linked to
using the site’s root as the path for the asset to include. Again, this will
depend on the way your site’s (sub)domain and path are configured, but here some
examples (in Markdown) of how you could do this using the `site.url` variable in
a post.

Including an image asset in a post:

{% highlight text %}
… which is shown in the screenshot below:
![My helpful screenshot]({% raw %}{{ site.url }}{% endraw %}/assets/screenshot.jpg)
{% endhighlight %}

Linking to a PDF for readers to download:

{% highlight text %}
… you can [get the PDF]({% raw %}{{ site.url }}{% endraw %}/assets/mydoc.pdf) directly.
{% endhighlight %}

<div class="note">
  <h5>ProTip™: Link using just the site root URL</h5>
  <p>
    You can skip the <code>{% raw %}{{ site.url }}{% endraw %}</code> variable
    if you <strong>know</strong> your site will only ever be displayed at the
    root URL of your domain. In this case you can reference assets directly with
    just <code>/path/file.jpg</code>.
  </p>
</div>

## Displaying an index of posts

It’s all well and good to have posts in a folder, but a blog is no use unless
you have a list of posts somewhere. Creating an index of posts on another page
(or in a [template](../templates/)) is easy, thanks to the [Liquid template
language](http://wiki.shopify.com/Liquid) and its tags. Here’s a basic example of how
to create a list of links to your blog posts:

{% highlight html %}
<ul>
  {% raw %}{% for post in site.posts %}{% endraw %}
    <li>
      <a href="{% raw %}{{ post.url }}{% endraw %}">{% raw %}{{ post.title }}{% endraw %}</a>
    </li>
  {% raw %}{% endfor %}{% endraw %}
</ul>
{% endhighlight %}

Of course, you have full control over how (and where) you display your posts,
and how you structure your site. You should read more about [how templates
work](../templates/) with Jekyll if you want to know more.

## Post excerpts

Each post automatically takes the first block of text, from the beginning of the content
to the first occurrence of `excerpt_separator`, and sets it as the `post.excerpt`.
Take the above example of an index of posts. Perhaps you want to include
a little hint about the post's content by adding the first paragraph of each of your
posts:

{% highlight html %}
<ul>
  {% raw %}{% for post in site.posts %}{% endraw %}
    <li>
      <a href="{% raw %}{{ post.url }}{% endraw %}">{% raw %}{{ post.title }}{% endraw %}</a>
      <p>{% raw %}{{ post.excerpt }}{% endraw %}</p>
    </li>
  {% raw %}{% endfor %}{% endraw %}
</ul>
{% endhighlight %}

If you don't like the automatically-generated post excerpt, it can be overridden by adding
`excerpt` to your post's YAML front-matter. Completely disable it by setting
your `excerpt_separator` to `""`.

## Highlighting code snippets

Jekyll also has built-in support for syntax highlighting of code snippets using
Pygments, and including a code snippet in any post is easy. Just use the
dedicated Liquid tag as follows:

{% highlight text %}
{% raw %}{% highlight ruby %}{% endraw %}
def show
  @widget = Widget(params[:id])
  respond_to do |format|
    format.html # show.html.erb
    format.json { render json: @widget }
  end
end
{% raw %}{% endhighlight %}{% endraw %}
{% endhighlight %}

And the output will look like this:

{% highlight ruby %}
def show
  @widget = Widget(params[:id])
  respond_to do |format|
    format.html # show.html.erb
    format.json { render json: @widget }
  end
end
{% endhighlight %}

<div class="note">
  <h5>ProTip™: Show line numbers</h5>
  <p>
    You can make code snippets include line-numbers by adding the word
    <code>linenos</code> to the end of the opening highlight tag like this:
    <code>{% raw %}{% highlight ruby linenos %}{% endraw %}</code>.
  </p>
</div>

These basics should be enough to get you started writing your first posts. When
you’re ready to dig into what else is possible, you might be interested in doing
things like [customizing post permalinks](../permalinks/) or using [custom
variables](../variables/) in your posts and elsewhere on your site.
