---
title: 3.Front Matter
---
Front matter is a snippet of [YAML](http://yaml.org/) which sits between two
triple-dashed lines at the top of a file. Front matter is used to set variables
for the page, for example:

![Front](http://localhost:4000/assets/front1.jpg)

Front matter variables are available in Liquid under the `page` variable. For
example to output the variable above you would use:

![pagenumber](http://localhost:4000/assets/front2.jpg)

## Use front matter

Let's change the `<title>` on your site to populate using front matter in `index.html`:

![Index](http://localhost:4000/assets/front3.jpg)

You may still be wondering why you'd output it this way as it takes
more source code than raw HTML. In this next step, you'll see why we've
been doing this.