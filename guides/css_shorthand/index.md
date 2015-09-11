---
title: CSS shorthand guide
readiness: 'Ready to Use'
summary: "This short article covers the various bits of CSS shorthand you'll encounter in your day to day work. It expands on the basic information found in the \nGetting Started with CSS tutorial.\n"
tags:
  - Guides
  - CSS
uri: 'guides/css shorthand'

---
## <span>Summary</span>

This short article covers the various bits of CSS shorthand you'll encounter in your day to day work. It expands on the basic information found in the Getting Started with CSS tutorial.

## <span>Border</span>

`border` allows you to set border width, style and, color all in one single property. So for example:

``` css
border: 1px solid black;
```

 is equivalent to the following three rules:

``` css
border-width: 1px;
border-style: solid;
border-color: black;
```

 You can also break these down further into even more specific rules, for a single border of the element it is applied to, like so:

``` css
border-left: 1px solid black;
border-right: 1px solid black;
border-top: 1px solid black;
border-bottom: 1px solid black;
```

 or even:

``` css
border-left-width: 2px;
border-left-style: solid;
border-left-color: black;
```

 You will very rarely want to go this granular; you will probably use simply `border` or `border-left/-right/-top/-bottom` in most cases. The more granular options will likely be used only if you want to override an earlier border declaration.

## <span>Margin, padding, outline</span>

Shorthand for `margin`, `padding`, and `outline` all works in the same way. Consider the following `margin` rule:

``` css
div.foo {
  margin-top: 1em;
  margin-right: 1.5em;
  margin-bottom: 2em;
  margin-left: 2.5em;
}
```

 Such a rule could also be written as:

``` css
div.foo {
  margin: 1em 1.5em 2em 2.5em;
}
```

 These types of property can take less than four values too, as follows:

1.  Same value applied to all four sides — `margin: 2px;`
2.  First value applied to the top and bottom, second to the left and right — `margin: 2px 5px;`.
3.  First and third values applied to the top and bottom respectively, second value applied to the left and right — `margin: 2px 5px 1px;`.

## <span>Font</span>

You can specify the font size, weight, style, family, and line height using one line of shorthand. Consider the following CSS:

``` css
font-weight: bold;
font-style: italic;
font-variant: small-caps;
font-size: 1.5em;
line-height: 200%;
font-family: Georgia, "Times New Roman", serif;
```

 You could specify all of this using the following line:

``` css
font: bold italic small-caps 1.5em/200% Georgia, "Times New Roman", serif;
```

 Note that it doesn't really matter about the order of many of these, although you should make sure that `font-size`/`line-height` and `font-family` come in the positions shown above; in addition, `font-size` and `font-family` should be specified. If not, this shorthand may not work in some browsers.

Note also that if `font-weight`, `font-style` or `font-variant` are not specified, their values default to `normal`.

## <span>Background</span>

In CSS 2, you can specify background color, background image, image repeat and image position with one line of CSS. Take the following:

``` css
background-color: #000;
background-image: url(image.gif);
background-repeat: no-repeat;
background-position: top left;
background-attachment: fixed;
```

 This can all be represented using the following shorthand:

``` css
background: #000 url(image.gif) no-repeat top left fixed;
```

 Note that if any of the values are left out, the following defaults are assumed:

``` css
background-color: transparent;
background-image: none;
background-repeat: repeat;
background-position: top left;
background-attachment: scroll;
```

### <span>Enhancements in CSS3</span>

CSS3 introduces three new properties: [`background-size`](http://www.w3.org/TR/css3-background/#the-background-size), [`background-origin`](http://www.w3.org/TR/css3-background/#the-background-origin), and [`background-clip`](http://www.w3.org/TR/css3-background/#the-background-clip). You can include them in the `background` shorthand like so:

``` css
background: #000 url(image.gif); no-repeat top left / 50% 20% border-box content-box;
```

 Notice the slash between `top left` and `50% 20%`; it separates the values for `background-position` and `background-size` since these two properties share some value units (lengths and percentage); without it we cannot distinguish which values are for which.

So if you want to include the `background-size` value in the shorthand syntax, you need to:

-   Explicitly include `background-position` values even if these are the same as the defaults (see above).
-   Write `background-position` values *before* `background-size` values.
-   Put a slash in between these two pairs of values.

Similarly, `background-origin` and `background-clip` share the same keyword as their values. These two also needs to be written in order: `background-origin` coming in first, and `background-clip` second.

If you only specify one `box` value (`border-box`, `padding-box`, or `content-box`), then the value applies to `background-origin` and `background-clip`.

Note: CSS3 gradients are a special, advanced value of `background-image` — aside from the syntactical difference, gradient values appear in exactly the same place in the shorthand as other `background-image` values, and work in the same way. For more on CSS3 gradients, you can read [CSS3 linear gradients](http://dev.opera.com/articles/view/css3-linear-gradients) and [CSS3 radial gradients](http://dev.opera.com/articles/view/css3-radial-gradients/) over at dev.opera.com.

## <span>List</span>

You can specify the list bullet type, position, and image on a single line. Take the following CSS:

``` css
list-style-type: circle;
list-style-position: inside;
list-style-image: url(bullet.gif);
```

 This is the equivalent of:

``` css
list-style: circle inside url(bullet.gif);
```

 Note that if any of the values are left out, the following defaults are assumed:

``` css
list-style-type: circle;
list-style-position: outside;
list-style-image: none;
```

## <span>Color</span>

When specifying hexadecimal color values, you can use shorthand if both hex values are the same for each color channel. For example, `#000` is equivalent to the longhand `#000000`. Let's look at a more complicated example too: `#6c9` is the same as `#66cc99`.