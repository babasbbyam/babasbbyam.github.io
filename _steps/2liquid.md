---

title: 2. Liquid
---
Liquid is where Jekyll starts to get more interesting. Liquid is a templating
language which has three main parts: object , tag ,and filter.


## Object
Objects tell Liquid where to output content.They're denoted by double curly
braces: For Example

![Brace](http://localhost:4000/assets/liquid1.jpg)
 
Output will be Title of the page.

## Tags

Tags create the logic and control flow for templates. They are denoted by curly
braces and percent signs.For Example:

![tags](http://localhost:4000/assets/liquid2.jpg)

Outputs the sidebar if `page.show_sidebar` is true.

## Filters

Filters change the output of a Liquid object. They are used within an output
and are separated by a `|`. For example:

![Filter](http://localhost:4000/assets/liquid3.jpg)

## Use Liquid

Now it's your turn, change the Hello World! on your page to output as lowercase:

![Example](http://localhost:4000/assets/liquid4.jpg)

It may not seem like it now, but much of Jekyll's power comes from combining
Liquid with other features. 

In order to see the changes from `downcase` Liquid filter, we will need to add front matter. 

That's next. Let's keep going.
