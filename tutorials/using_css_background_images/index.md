---
title: 'Using CSS background images'
readiness: 'Ready to Use'
summary: 'This article covers CSS backgrounds in detail: background color, image, repeat, attachment, and position. Near the end, it also looks at advanced techniques such as CSS sprites.'
tags:
  - Tutorials
  - CSS
uri: 'tutorials/using css background images'

---
## Summary

This article covers CSS backgrounds in detail: background color, image, repeat, attachment, and position. Near the end, it also looks at advanced techniques such as CSS sprites.

## Introduction

Admit it! Since the first article in the [Web Standards Curriculum](http://www.w3.org/wiki/Web_Standards_Curriculum), you’ve been excited to learn how to make your site look fierce and fabulous. Maybe you even skipped ahead to this section?

Background images are all about making your site look stunning, but you might be surprised how closely they build upon the fundamental concepts you have already learned.

As you previously learned from an earlier article in this series, one of the most important changes that comes with CSS is the ability to separate *presentation*, or the way things look, from *semantics*, or what things mean. The CSS background image is among the most important tools you have at your disposal, because it lets you apply decorative images to particular parts of your HTML without adding any extra weight to your HTML. Previously, authors (like you!) were forced to fill their code with `img` tags to achieve the same effect.

CSS and in particular the `background` property keep your HTML free from presentational clutter. Redesigns and other transitions, in the life of sites built with modern methods, can then be completed much more efficiently. You can update your entire site by changing only the style sheet, rather than recoding every HTML page. Depending on the size of your site, this can be a substantial time savings.

In this article, you will learn the basics of how CSS background images work. You will see how to apply a background image via CSS, adjust its placement, tile it vertically or horizontally and combine background images using [CSS Sprites](http://www.alistapart.com/articles/sprites/) to improve [site performance](http://developer.yahoo.com/performance/index.html).

## How does it work?

The CSS for backgrounds is split into several different properties. Using these properties, such as `position` and `color`, you can begin to control the look and feel of your page. In this article, you will go through CSS background images in detail, building an alert message as an example, step by step.

First, review the different properties you can use.

### Background Properties

<table>
<col width="33%" />
<col width="33%" />
<col width="33%" />
<thead>
<tr class="header">
<th align="left">Property</th>
<th align="left">Definition</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><code>background-color</code></td>
<td align="left">Sets the background color of the HTML element.</td>
<td align="left"><p>There are several ways to indicate <code>background-color</code>, including RGB values and keywords. Most people use hexadecimal notation, a pound/hash symbol (#) followed by six characters. The first pair indicates the red levels, and the second and third indicate the green and blue levels respectively—<code>#RRGGBB</code>.</p>
<p>Many color picker tools will help you find the hexadecimal notation of a given color. Pure red, for example would be #FF0000.</p>
<p><img src="/assets/public/f/fb/color_pi.jpg" alt="Photoshop color picker displays the hex value of your color" /></p>
<p>Valid values include a <code>colour</code> value, <code>transparent</code>, or <code>inherit</code>.</p></td>
</tr>
<tr class="even">
<td align="left"><code>image</code></td>
<td align="left">Indicates the path<em>or URL</em> of the background image.</td>
<td align="left"><p>Set the <code>background-image</code> by showing the browser where to find the image, using the URL. For example; <code>url(alert.png)</code>. Note that the path is prefaced with they keyword <code>url</code> and wrapped in parenthesis. This syntax is important to the browser understanding that you mean to indicate a location. If your url contains special characters or white space, you may have to use apostrophes or quotations around the url inside of the parentheses.</p>
<p>Valid values include a <code>URL</code>, <code>none</code>, or <code>inherit</code>.</p></td>
</tr>
<tr class="odd">
<td align="left"><code>repeat</code></td>
<td align="left">Indicates in which direction the background image should be tiled.</td>
<td align="left"><p><br /> Images can be tiled vertically, horizontally, or both, to fill the entire width or height of an HTML element. Use <code>background-repeat</code> to instruct the browser to repeat a background image.</p>
<p>Valid values include <code>repeat</code>, <code>repeat-x</code>, <code>repeat-y</code>, and <code>no-repeat</code>.</p>
<p><br /></p></td>
</tr>
<tr class="even">
<td align="left"><code>attachment</code></td>
<td align="left">Sets the behavior of the background image when the user scrolls.</td>
<td align="left"><p>Images can either scroll with their content, or stay fixed in place in the view screen. Valid values include <code>scroll</code>, <code>fixed</code>, and <code>inherit</code>.</p></td>
</tr>
<tr class="odd">
<td align="left"><code>position</code></td>
<td align="left">Tells the browser where to position the background image.</td>
<td align="left"><p>Images can be displayed anywhere within the borders of the HTML element on which they are applied. Use <code>background-position</code> to precisely place your images for visual effect and layering.</p>
<p>There are many useful ways to indicate background position, keywords, and numeric values. Keywords (such as <code>top</code> and <code>bottom</code>) are very useful and easy to read. Pixel values are very precise, but they do not adapt to changing heights and widths. Negative pixel values are useful when using CSS sprites, as you will see later.</p>
<p>When percentages and pixels are used, the starting point is always the top left corner of the HTML element, although the way image positioning works with pixels and percentages is rather different. Pixels always move the image a set number of pixels towards the bottom and right of the containing box (or towards the top and left if they are negative values), regardless of the size of the image and the containing box. Percentages, on the other hand, move the image a percentage of the difference between the containing box size, and the image size. If the image and the containing box are the same size, percentages will not move the image at all.</p>
<p>Valid values include <code>length</code> (generally in pixels), <code>percentage</code> (of the width of the element), and the keywords <code>top</code>, <code>right</code>, <code>bottom</code>, <code>left</code>, and <code>center</code>. Note that center can be used to indicate both vertical and horizontal center. Note also that you can mix percentages and pixels in rules, but not keywords and pixels or keywords and percentages.</p></td>
</tr>
<tr class="even">
<td align="left"><code>background</code></td>
<td align="left">The shorthand property that can be used to describe all the other properties in one line.</td>
<td align="left"><p>Shorthand properties are very nifty indeed. Most developers use them to keep the CSS as lean as possible and group related properties. You can write a general rule using shorthand, and then override it as needed with specific properties.</p>
<p>The properties should always be indicated in the same order, to allow browsers to easily interpret the intended styles:</p>
<ol>
<li><code>color</code></li>
<li><code>url</code></li>
<li><code>repeat</code></li>
<li><code>attachment (very rarely used; may be omitted)</code></li>
<li><code>horizontal-position</code></li>
<li><code>vertical-position</code></li>
</ol>
<p>An example of this shorthand with all the properties used (except <code>attachment</code>) is as follows:</p>
<p><code>background: green url(logo.gif) no-repeat left top;</code></p></td>
</tr>
</tbody>
</table>

## Building an alert message

Now that you understand the basic syntax involved, you can walk through the process of building up a complete alert box example, which demonstrates all the aspects of working with background images.

### The design

Imagine a graphic designer has provided a visual mock-up of the alert message you want to create for your website. The alert has a light orange background color, to make it stand out from the surrounding paragraphs. It also has an alert icon ten pixels from the top left corner.

Note that the mockup has one line of text, but it might contain more in the future. One of the most important skills of the web developer is to anticipate how a design will evolve. Part of respecting the artistic vision for a site is thinking about consistency from launch to redesign. So the alert message could contain more than one line of text, or even multiple paragraphs, lists, or other HTML elements. Strive to be as element agnostic as possible. This will increase the likelihood of code reuse, and will enable you to set up the site to be as fast and efficient as it can be. The mockup looks like Figure 1.

![Final mock up](/assets/public/a/a1/alert_fi.jpg)

Figure 1: The graphic designer’s mockup of the alert box.

The designer has also provided the icon we are meant to use, as shown in Figure 2.

![Alert icon](/assets/public/9/9c/alert000.png)

Figure 2: The alert icon.

### The code

Based on what you have learned about CSS backgrounds in the first part of this article, you may already be envisioning how to build this alert message. I encourage you to try building it now, and then compare your work against the example below.

After building your alert box, follow the step by step instructions below. Each screenshot links to code examples, so you can check out the source file at each stage. Experiment with the code, by increasing or decreasing values, and try out alternatives. You may also want to follow along, writing each new line of code in a tool such as Opera Dragonfly or Firefox Firebug, so you can immediately see the results of each step.

#### Creating the CSS hook, or selector.

First you need to create a class `alert`, that enable you to hook up the CSS code. Create new CSS and HTML skeleton files, link the CSS style sheet to the HTML file, and add the following code to each:

Copy the following CSS and paste it into the style sheet:

``` css
.alert { ... }
```

 Copy the following HTML and paste it into the HTML document:

``` html
<p class="alert">
  <strong>Alert!</strong> The text of our alert message goes here.
</p>
```

 The code above styles the alert with a `class`, rather than an `id`, because that enables the possiblity for *more than one alert* in the page. For example, you may add alerts to a form element with several potential errors. The goal is to make your CSS as flexible as possible and constrain things to correspond to the design when building the HTML content.

At this point, you have a solid foundation in place, but the alert still looks like an ordinary paragraph because you have not yet added any styles. You will add some rules to style it next.

Note: I have intentionally chosen *not* to limit the class `alert` to paragraphs; alert boxes could easily contain other elements as well. You should leave as much flexibility as you can within your CSS.

#### Adding the background color

You already learned about using background color in text treatments in [*Text styling with CSS*](http://www.w3.org/wiki/Text_styling_with_CSS). The same principles apply to any HTML element and can be combined with background images to create visual effects. If the background color has neither been set nor inherited, it is, by default, transparent.

As shown below, you can add the light orange background color to the alert box to make it stand out from the text around it. It is important not to make the background color too dark, because you need to keep a reasonable level of [contrast between the text and the background color](http://www.w3.org/TR/2006/WD-WCAG20-20060427/guidelines.html#visual-audio-contrast). Add the following property inside the CSS rule:

``` css
.alert{
  background-color: #FFFFCC;
}
```

 The alert box now looks similar to Figure 3.

![Code](/assets/public/8/86/2_color0.gif)

Figure 3: An alert box with background color added.

#### Applying the background image

Next, you can add the background image to the alert. The path to the background image needs to be wrapped in `url()`, as shown in the code below. Add the highlighted line to the CSS rule:

``` css
.alert{
  background-color: #FFFFCC;

  /* Add the background image */
  background-image: url(alert.png);
}
```

 The alert box now looks like Figure 4.

![Code with background image](/assets/public/d/de/3_image0.gif)

Figure 4: The background image has been added, but the tiling looks wrong.

Remember that each background property has a default value—if you have not specified a value, the default will be applied. Notice that the image is tiling over the entire alert, much like mosaic tiles on a kitchen floor. What is the takeaway? Background images are set to repeat both horizontally and vertically by default. Repeating backgrounds are particularly useful for gradients and patterns that fill the screen or a particular HTML element, but that effect is *not* desired in this case.

#### Controlling background repeat

![Repeat horizontally and vertically](/assets/public/d/d6/repeat00.jpg)

Figure 5: Much like the background image, these tiles repeat both horizontally and vertically.

Reading specifications can certainly be intimidating, but the specification is a really good place to figure out how CSS is *supposed to work* before you delve into the myriad browser differences. Read the [colors and backgrounds portion of the W3C Specification](http://www.w3.org/TR/CSS21/colors.html) and try to find the keyword to use when you do not want a background image to be repeated. This strategy is used in the example below:

Note that there is a section for each background property including [background-repeat](http://www.w3.org/TR/CSS21/colors.html#propdef-background-repeat). Under **Value**, all of the possible choices are displayed, including; `repeat`, `repeat-x`, `repeat-y`, `no-repeat`, and `inherit`. By default (**initial**) background images are set to repeat. No direction is specified, which means that that the image will tile both horizontally and vertically. You have likely guessed that **`no-repeat`** is the value to set to prevent the image from tiling in either direction. Add the following highlighted line below to the CSS rule:

``` css
.alert{
  background-color: #FFFFCC;
  background-image: url(alert.png);

  /* Set the background repeat */
  background-repeat: no-repeat;
}
```

 The alert box now looks like Figure 6.

![Code for Step 4 background repeat](/assets/public/5/5a/4_repeat.gif)

Figure 6: The alert box, with a single copy of the background image (with no tiling).

Additionally, you can choose to repeat in both directions (like kitchen tiles) or in either direction. Gradients often repeat horizontally or vertically (see Figure 7). You do not need to know the size of the HTML element; you simply cut a slice from your gradient and set it to repeat in the direction you want; either x for horizontal, or y for vertical. Patterns often repeat in both directions and icons usually do not repeat. You will explore `background-repeat` further in a later example.

![repeat-x example](/assets/public/1/1e/repeat-x.jpg)

Figure 7: The greenish yellow tiles in this example repeat only horizontally.

Next, take a look at a practical example from my website. Review Figure 8.

![A tiny image is tiled horizontally to create a three color design across the top of my website.](/assets/public/7/7a/site_bac.jpg)

Figure 8: A repeating example from my website.

The CSS I used to add this decorative effect is relatively simple. I made the background repeat horizontally using `repeat-x`:

``` css
  body {
    /* set to repeat-x */
    background-repeat: repeat-x;
  }
```

#### Attachment

The `attachment` attribute allows you to specify how the background behaves when the user scrolls down the page. The default behavior is `scroll`, which causes the background image to scroll along with the content.

On the other hand, setting `background-attachment` to `fixed` causes the element to be stuck to the browser window, so it stays in the same place when the content inside the element it is attached to is scrolled. This creates some odd effects, which will only be apparent when you scroll over the attached HTML element. The W3C uses it to mark the status of their specifications. For example, the ["W3C Candidate Recommendation" image at top left](http://www.w3.org/TR/CSS21/colors.html#propdef-background-repeat). Scroll down the page and note that the image stays top left. It is attached to the `body` element, so it is always visible.

This step will have no effect on our display, because browsers set background images to scroll by default, but add it to the code anyway, to learn how the property is used. Add the highlighted line to the CSS rule:

``` css
.alert{
  background-color: #FFFFCC;
  background-image: url(alert.png);
  background-repeat: no-repeat;

  /* add background-attachment */
  background-attachment: scroll;
}
```

 As shown in Figure 9, the visual display of the alert box is not much different than it was before.

![Code for background attachment](/assets/public/3/38/5_attach.gif)

Figure 9: The display has not changed.

#### Positioning the image

Positioning is the fine tuning that enables you to place background images exactly where desired, both horizontally and vertically, within the HTML element. This property takes keyword and number values such as` top`, `center`, `right`, `100%`, `-10%`, `50px` and `-30em`.

Figure 10 shows the values you might use to place your background images in different positions.

![Examples of possible background positions](/assets/public/d/da/backgrou.gif)

Figure 10: Various examples of background position using keywords, percentages, and pixels.

The code below positions the background image. The goal is to position it in the top left corner, but not touching the sides, so you need to offset it by 10 pixels from both the top and left. This is accomplished by adding the following highlighted line to the CSS rule:

``` css
.alert{
  background-color: #FFFFCC;
  background-image: url(alert.png);
  background-repeat: no-repeat;
  background-attachment: scroll;

  /* Add the background position */
  background-position: 10px 10px;
}
```

 The first value is the horizontal offset, the second is the vertical. In this case the values are the same. After making these changes, your alert box should look like Figure 11.

![Code with background position](/assets/public/f/f1/6_positi.gif)

Figure 11: Using CSS positioning to set the location of the background image.

Tip: Choose either keywords or number values, but do not combine them. Older browsers may ignore your declaration if you use both at once. Using `right` and `bottom` will achieve the same effect as using `100%` horizontally or vertically, respectively.

#### Using shorthand to pull the whole thing together like a pro

As you have learned, certain CSS properties can be grouped together. Background and all of its sub-properties can be grouped in CSS rules. The CSS code described so far can be rewritten in a shortened form, as follows:

``` css
  .alert{
    /* change to the shorthand form */
    background: #FFFFCC url(alert.png) no-repeat scroll 10px 10px;
  }
```

 Tip: When grouping sub-properties of `background`, always put the properties in the following order. This is important for both cross-browser compatibility and style sheet organization and maintenance:

1.  `color`
2.  `image`
3.  `repeat`
4.  `attachment`
5.  `horizontal` position
6.  `vertical` position

Try replacing the old CSS code in your document with the shorthand shown above. After updating it, the example should look exactly the same (see Figure 12).

![Finished product](/assets/public/e/e3/7_finish.gif)

Figure 12: The shorthand works like a charm!

### Experimenting with the code

The best way to remember all the nuances of CSS is to test the options yourself. Try changing some of the properties in the example, and see how different values affects the display. Set the `background-position` to `100% 100%`, and notice that it provides the same result as using the `right` and `bottom` keywords. What about if you change it to `-5px 0`? Why do you think part of the image is hidden?

### Testing for quality

Testing is extremely important to providing a good user experience. Just because the site looks good on your machine with your specific configuration does not mean that it will look good in every browser. Follow these basic minimum steps when testing your alert box:

-   Increase or decrease the amount of text inside the alert.
-   Increase the text size in your browser at least two levels. Determine if it is better to use ems to position our image. Test what happens when you increase the text size.
-   Apply the `class` alert to other elements such as `div`, `p`, `ul`, `strong`, or `em`. How can you change the code to make the class agnostic?
-   Include several paragraphs and a list inside an alert `div`. Does the code still work?
-   Verify the alert visually in the [Grade 1 browsers](http://www.bbc.co.uk/guidelines/futuremedia/technical/browser_support.shtml#support_table) (also known as A-grade browsers). My advice is to write the code for good browsers and then adapt it for Internet Explorer--once the code works.

Rigorous testing is part of learning to write CSS. The more careful you are while learning, the faster you will be able to code.

## Sprites

Users want it all. They want your site to be glamorous, interactive, and also fast. However, including large quantities of CSS background images can slow your site down considerably. The more HTTP requests you make, the slower your site will be (an HTTP request occurs whenever your computer is accessing a website and needs to ask the server to send it another asset in the site design, such as a CSS file or image... each additional request means a longer loading time for the site).

To get around this limitation, you can combine related icons into a single image, known as [CSS Sprites](http://www.alistapart.com/articles/sprites). The `background-position` property allows you to then place the image in the appropriate positions so the icons display through the *window* of the HTML element that the CSS sprites are attached to.

In Figure 13, notice that to display the earth icon through the HTML window, you can place the image using `left top`. To move the position of the image so the alert icon is displayed, the background position needs to be changed to `-80px 0`. The negative horizontal value pulls the image to the left.

![Only the part of the background image which is inside the HTML element is visible](/assets/public/7/7a/sprite_6.gif)

Figure 13: Use CSS Sprites to reduce HTTP requests.

Note: If you set negative background positions, Safari will repeat your image, even if you’ve specified `no-repeat`. This is a consideration as you start working with background images to create more complicated layouts.

### A complex sprite and background image example

Next, take a look at how you can leverage CSS sprites. Suppose a friendly designer sent us an new mockup. This one illustrates a list of links on the landing page of a blog. It points to the bloggers’ LinkedIn profile, RSS feed, Flickr photos, and bookmarks. As you evaluate each link, notice that there is a gradient starting in the center as white and transitioning to gray at the top and bottom of the link. And to further complicate things, the designer asked if we could make each link plain white with no curve when visitors hover over the link, as shown in Figure 14.

![List mockup](/assets/public/b/b5/List0000.gif)

Figure 14: The new design mockup.

The logos could be included using `img` elements in the markup. However, using CSS sprites is a much better solution. The sprites load faster because only one image must load (not four), and it declutters your HTML, by reducing the amount of markup needed.

#### Creating the sprite

The first step involves cutting out the four logos and creating the sprite set, as shown in Figure 15.

![Logos sprite](/assets/public/4/4b/sprite_l.gif)

Figure 15: The sprite set.

You also need to cut out a 1 pixel wide slice of the gradient. For the sake of visibility, I have cut out a slightly larger slice, but in a real-world site project you only need a one pixel image (see Figure 16).

![Gradient background](/assets/public/6/66/sprite_g.jpg)

Figure 16: The slice used for the gradient background.

The HTML that creates the list is an unordered list containing links. Note the empty `span` elements inside the links. It is very important not to have fixed `height` and `width` on elements that contain text. After all, you have no idea how large the text will be. What happens if the site is translated to German? You can use these extra spans to display the logos. As an alternative, you may decide that you do not want to have extraneous non-semantic markup cluttering up your HTML. In this case, you will need to use a larger sprite and leave white space between the icons. Keep in mind that this strategy is slower for users on slow connections, especially those using mobile phones to view the site. The code for the list is shown below. Copy it and then paste it into an HTML document:

``` html
  <ul class="navigation">
    <li id="resume">
      <a href="#">Resume</a>
    </li>
    <li id="rss">
      <a href="#">RSS Feed</a>
    </li>
    <li id="photos">
      <a href="#">Photos</a>
    </li>
    <li id="links">
      <a href="#">Links</a>
    </li>
  </ul>
```

 Add the following CSS to a new CSS file, and link it to the HTML document:

``` css
.navigation, .navigation li {
  margin:0;
  padding:0;
}

.navigation li {
  border-top: 1px solid white;
  list-style-type:none;
}

.navigation li a {
  background: #E2E2E2 url(sprite_gradient_bkg.jpg) repeat-x left center;
  padding:20px;
  display:block ;
  font-family: Arial, Helvetica, sans-serif;
  color:#333;
  font-size:18px;
  text-decoration:none;
}

/* hover effects */

.navigation li a:hover, .navigation li a:focus {
  background: transparent none;
}
```

 The CSS utilizes both background images. First, take a look at the gradient background image. There are three interesting things to notice:

1.  The image repeats horizontally (`repeat-x`.) This tiling enables you to make such a small image spread across the entire list.
2.  The image is centered vertically. You want the round bit of the image to appear in the middle of the list item, so you should use a background position of `left center`.
3.  In the CSS, I’ve applied a background color that is the same gray as the gray in the gradient image. This ensures, if the element grows, it will not look broken. For more information about this kind of technique, I recommend reading [Bulletproof Web Design](http://www.simplebits.com/publications/bulletproof/) by Dan Cederholm.

The last line means that the element should not display a background color or image when the visitor hovers their cursor over it, or focuses on the element using the keyboard. You may be wondering why I applied the background properties to the link rather than the list item. The answer is that Internet Explorer 6 and earlier do not support pseudo classes like `hover` on elements other than links. I’ve made the adjustment in the code to accommodate this constraint.

Next you can create the CSS for the little logos. As usual, you can start by defining the most general case for all `span` elements within your navigation module. It is here that you define the image to be used by all spans, the repeat setting, and the background position (each is different, so you can use the first one). You can use shorthand for this rule. Note that CSS comments divide the sections of our code into manageable chunks. Add the following code to the bottom of the CSS file:

``` css
/* general case */

.navigation span {
  background:url(sprite_logo.gif) no-repeat left top;
  height:15px;
  width: 15px;
  margin-right:20px;
  display:-moz-inline-box;
  display:inline-block;
  vertical-align: middle;
}
```

 With the basic formatting completed, you can now define the exceptions, or *what is different* about each specific logo. In this case, the only CSS that changes is the `background-position`. Each respective list item needs to have the image moved 15 pixels more to the left, because each of the logo images are 15 pixels wide. Add the following to the bottom of the CSS file:

``` css
/* exceptions */

#rss span {
  background-position: -15px 0;
}

#photos span {
  background-position: -30px 0;
}

#links span {
  background-position: -45px 0;
}
```

 This example might seem intimidating at first. Keep your focus on the background images. In this case, using a negative pixel value pulls the background image left, so that the relevant part of the image is displayed. Positive values move the background image down and right, while negative values pull the image up and to the left.

Experiment with the background position values in the [finished example](http://dev.opera.com/articles/view/31-css-background-images/sprite.html), to better understand how to adjust sprite positioning.

## Usage

     on 02/10/2014 arond 1500 central std time:

hoffmant99 made minor changes to make sprite example work, though the student(reader of this page) needs to be aware that the file names don't match. This can be fixed locally, change the name from "sprite\_logo" to "sprite\_l" and" sprite\_gradient\_bkg.jpg" to sprite\_g.jpg".

## See also

### External resources

-   [Performance and HTTP requests on YDN](http://developer.yahoo.com/performance/rules.html#num_http)
-   [CSS2 Specification—Colors and Backgrounds](http://www.w3.org/TR/REC-CSS2/colors.html)
-   [CSS Sprites—Image Slicing’s Kiss of Death](http://www.alistapart.com/articles/sprites)
-   [Bulletproof Web Design](http://www.simplebits.com/publications/bulletproof/)—My favourite book

### Image credits

-   [The Tiles](http://www.flickr.com/photos/dimsumdarren/1342305614/), by DimsumDarren
-   [little glass tiles](http://www.flickr.com/photos/emdot/6099842/), by emdot

### Exercise Questions

-   A paragraph is 40px by 180px and your background image is 60px by 200px. Will you see the entire image or only part of it? Why?
-   You want an image to be positioned in the bottom left corner of the `blockquote` element—please fill in the correct values.

        blockquote{background: yellow url(quote.png) no-repeat scroll ____ ____ ;}

-   Say you wanted each `h2` in your document with a `class` of "question" to have a gradient pattern applied. Would you use `repeat-x`, `repeat-y`, `no-repeat`, or `repeat` to achieve something similar to the example below? Why?

![logos sprite](/assets/public/2/24/exercise_example.gif)

-   What would be the background position of the example in question number 3? How could you creatively use a background colour to be sure the background could expand to any height? Why is this important?
-   What shorthand can you use to remove all background properties?
-   What is the purpose of CSS sprites?
