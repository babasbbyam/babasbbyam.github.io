---
title: 8. Blogging
---

You might be wondering how you can have a blog without a database. In true
Jekyll style, blogging is powered by text files only.

## Posts

Blog posts live in a folder called `_posts`. The filename for posts have a
special format: the publish date, then a title, followed by an extension.

Create your first post at `_posts/2018-08-20-bananas.md` with the
following content:

![Banana](http://localhost:4000/assets/postbanana.jpg)

This is like the `about.md` you created before except it has an author and
a different layout. `author` is a custom variable, it's not required and could
have been named something like `creator`.

## Layout

The `post` layout doesn't exist so you'll need to create it at
`_layouts/post.html` with the following content:

![Post](http://localhost:4000/assets/posthtml.jpg)

This is an example of layout inheritance. The post layout outputs the title,
date, author and content body which is wrapped by the default layout.

Also note the `date_to_string` filter, this formats a date into a nicer format.

## List posts

There's currently no way to navigate to the blog post. Typically a blog has a
page which lists all the posts, let's do that next.

Jekyll makes posts available at `site.posts`.

Create `blog.html` in your root (`/blog.html`) with the following content:

![Blog](http://localhost:4000/assets/bloghtml.jpg)

There's a few things to note with this code:

* `post.url` is automatically set by Jekyll to the output path of the post
* `post.title` is pulled from the post filename and can be overridden by
setting `title` in front matter
* `post.excerpt` is the first paragraph of content by default

You also need a way to navigate to this page through the main navigation. Open
`_data/navigation.yml` and add an entry for the blog page:

![Nav data](http://localhost:4000/assets/navyml.jpg)

## More posts

A blog isn't very exciting with a single post. Add a few more:

`_posts/2018-08-21-apples.md`:

![Apple](http://localhost:4000/assets/postapple.jpg)

`_posts/2018-08-22-kiwifruit.md`:

![Kiwi](http://localhost:4000/assets/postkiwi.jpg)

Open <a href="http://localhost:4000" target="_blank" data-proofer-ignore>http://localhost:4000</a> and have
a look through your blog posts.

![Result](http://localhost:4000/assets/resultbloghtml.jpg)


Next we'll focus on creating a page for each post author.