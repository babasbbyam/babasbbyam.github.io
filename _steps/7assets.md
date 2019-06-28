---

title: 7. Assets
---

Using CSS, JS, images and other assets is straightforward with Jekyll. Place
them in your site folder and they’ll copy across to the built site.

Jekyll sites often use this structure to keep assets organized:

![Asset](http://localhost:4000/assets/assetterminal.jpg)

## Sass

The inline styles used in `_includes/navigation.html` is not a best practice,
let's style the current page with a class instead.

![Sass](http://localhost:4000/assets/assetcss.jpg)

You could use a standard CSS file for styling, we're going to take it a step
further by using [Sass](https://sass-lang.com/). Sass is a fantastic extension
to CSS baked right into Jekyll.

First create a Sass file at `/assets/css/styles.scss` with the following content:

![Stylecss](http://localhost:4000/assets/stylescss.jpg)

The empty front matter at the top tells Jekyll it needs to process the file. The
`@import "main"` tells Sass to look for a file called `main.scss` in the sass
directory (`_sass/` by default which is directly under root folder of your website).

At this stage you'll just have a main css file. For larger projects, this is a
great way to keep your CSS organized.

Create a Sass file at `/_sass/main.scss` with the following content:

![Maincss](http://localhost:4000/assets/mainscss.jpg)

You'll need to reference the stylesheet in your layout.

Open `_layouts/default.html` and add the stylesheet to the `<head>`:

![Default](http://localhost:4000/assets/defaultcss.jpg)

oad up <a href="http://localhost:4000" target="_blank" data-proofer-ignore>http://localhost:4000</a>
and check the active link in the navigation is green.

![Result](http://localhost:4000/assets/resultgreen.jpg)

Next we're looking at one of Jekyll's most popular features, blogging.