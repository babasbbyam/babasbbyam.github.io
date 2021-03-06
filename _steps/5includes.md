---

title: 5. Includes
---
The site is coming together; however, there's no way to navigate between
pages. Let's fix that.

Navigation should be on every page so adding it to your layout is the correct
place to do this. Instead of adding it directly to the layout, let's use this
as an opportunity to learn about includes.

## Include tag

The `include` tag allows you to include content from another file stored
in an `_includes` folder. Includes are useful for having a single source for
source code that repeats around the site or for improving the readability.

Navigation source code can get complex so sometimes it's nice to move it into an
include. 

## Include usage

Create a file for the navigation at `_includes/navigation.html` with the
following content:

![navigation](http://localhost:4000/assets/navinclude.jpg)

Try using the include tag to add the navigation to `_layouts/default.html`:

![default](http://localhost:4000/assets/defaultinclude.jpg)

Open <a href="http://localhost:4000" target="_blank" data-proofer-ignore>http://localhost:4000</a>
in your browser and try switching between the pages.

## Current page highlighting

Let's take this a step further and highlight the current page in the navigation.

`_includes/navigation.html` needs to know the URL of the page it's inserted into
so it can add styling. Jekyll has useful variables available
one of which is `page.url`.

Using `page.url` you can check if each link is the current page and color it red
if true:

![redline](http://localhost:4000/assets/redlineinclude.jpg)

Take a look at <a href="http://localhost:4000" target="_blank" data-proofer-ignore>http://localhost:4000</a>
and see your red link for the current page.

![result](http://localhost:4000/assets/redlineresultinclude.jpg)

There's still a lot of repetition here if you wanted to add a new item to the
navigation or change the highlight color. In the next step we'll address this.



