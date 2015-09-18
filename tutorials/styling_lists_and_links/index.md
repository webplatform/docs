---
title: 'Styling lists and links'
readiness: 'Ready to Use'
summary: 'This article covers styling fundamentals for lists and links.'
tags:
  - Tutorials
  - CSS
uri: 'tutorials/styling lists and links'

---
## Summary

This article covers styling fundamentals for lists and links.

## Introduction

Many elements on a webpage are a little bit "forgiving" in terms of design — if they're not "just right" it doesn't matter too much. With lists and links it's a different story — if you don't get them right, you can cause some serious problems for people trying to use your website.

Links in particular have some key style requirements and user expectations. Poorly styled links can ruin the user experience on a website, as people have to stop and think about where to click. In the worst case, a user might not even be able to tell which items on the page are actually links.

In this article we'll look at the core skills you need to create robust list and link styles. We'll also discuss some ways to avoid key pitfalls of these elements and produce a final result that will work across different browsers, and be accessible to users with disabilities.

## Styling Lists

First, let's go through the basics of styling lists with CSS, before then moving on to look at some slightly more complicated techniques.

### Basic bullets and numbers

The fundamental thing to consider when creating a list style is what form of bullet or numbering you want to use. You might also choose to remove the bullets and numbers completely. As you learned in the [HTML Lists](/guides/html_lists) article, there are many options available, set using the `list-style-type` property.

For example, to set all unordered lists on your site to use square bullets, use this CSS:

    ul li {
      list-style-type: square;
    }

Which will produce something like Figure 1:

![Screenshot of a list with square bullets](//static.webplatform.org/6/66/square-b.gif)

*Figure 1: Unordered list with square bullets.*

Some common list types are shown in Figure 2:

![Screenshot of some common list types.](//static.webplatform.org/f/fe/referenc.gif)

*Figure 2: Common list styles.*

Note that the bullets and numbers will be rendered using the `color` which is set for or inherited by the `li`. If you need the bullet to be a different colour from the text, you will need to use an image instead, or work around the issue using other elements within the list items (this may be easy if all the items are links, for example).

### Custom bullets using images

The standard set of bullets are enough for basic content, however it is a common design request to replace them with a custom image.

The CSS specification does include the `list-style-image` property for adding a custom list image. However, the property has limited positioning options for the background image, and in some circumstances doesn't work at all in IE. So it has become a far more common practice to simply set a background image on the list items.

Let's imagine you have a list of RSS feeds and you want to change the bullet to the standard orange RSS icon. We'll give the list the class "rss" to differentiate it from other lists:

    <ul class="rss">
      <li><a href="http://example.com/rss.xml">News</a></li>
      <li><a href="http://example.com/rss.xml">Sport</a></li>
      <li><a href="http://example.com/rss.xml">Weather</a></li>
      <li><a href="http://example.com/rss.xml">Business</a></li>
      <li><a href="http://example.com/rss.xml">Entertainment</a></li>
      <li><a href="http://example.com/rss.xml">Funny News</a></li>
    </ul>

First we'll set the list to have no `list-style-type` and remove the margin and padding. Then, simply add a background image to each list item, some left padding to move the text over to let the image show through, and some bottom padding to space out the list items:

    .rss {
      margin: 0;
      padding: 0;
      list-style-type: none;
    }

    .rss li {
      background: #fff url("icon-rssfeed.gif") 0 3px no-repeat;
      padding: 0 0 5px 15px;
    }

This will produce a list with the RSS image instead of bullets, as seen in Figure 3:

![Screenshot of a list with the bullets replaced with images](//static.webplatform.org/d/dc/image-bu.gif)

*Figure 3: The list with image bullets.*

Bear in mind that the background image is positioned using pixels for a precise placement. Depending on the design you are creating, you might also be able to use `%`, `em`s or keywords. Just be careful when your design features content that might cause a list item to wrap over several lines—if you set the background to vertical `center` or `50%` it can look quite strange, as shown in Figure 4:

![Screenshot showing the way the vertically-centred bullet will sit in the middle of the text, instead of being centred to the first line of text.](//static.webplatform.org/4/45/image-bv.gif)

*Figure 4: A demonstration of vertically-centred bullet images on a multi-line list item.*

By setting the image to sit at the top of the list item, you maintain the default bullet behaviour (where the bullet sits on the first line)—see Figure 5:

![Screenshot of top-positioned bullet images.](//static.webplatform.org/9/96/image-bw.gif)

*Figure 5: A demonstration of top-aligned bullet images on a multi-line list item.*

### List margins and padding

Clever use of margins and padding can make lists look much more polished and professional, but you need to know what you are doing, and also bear in mind that the situation differs between different types of list. In this section I'll take you through applying sensible margins and padding to the two most common types of list.

#### Unordered lists

One thing you will probably notice quite quickly is that the default style for lists indents them more than the default style for paragraphs—see Figure 6:

![Screenshot of default list styles with a larger left indent than paragraphs.](//static.webplatform.org/a/ad/list-ind.gif)

*Figure 6: Default styled lists are indented on the left.*

If you want your unordered list items to sit at the same left-align point as the rest of your content, you will need to set some styles to control the indentation to your liking. Different browsers require different settings—some need the margin removed, others need the padding removed. So, to reset for all browsers, reset both:

    ul {
      margin: 0;
      padding: 0;
    }

This may not have the effect you were expecting, as it will get the *text* to sit flush left but the bullets will sit outside the text, as shown in Figure 7:

![Screenshot of bullets sitting outside the text.](//static.webplatform.org/5/51/list-ine.gif)

*Figure 7: Bullets are positioned to the left of the text.*

So, to align the *bullets* to the left you can now set a margin on the list items to line things up:

    ul {
      margin-left: 0;
      padding-left: 0;
    }

    ul li {
      margin-left: 1em;
    }

...at this point you will still find a pixel-level difference between browsers but the effect is basically as consistent as possible—see Figure 8:

![Screenshot of bullets left-aligned closely with paragraphs.](//static.webplatform.org/3/38/list-inf.gif)

*Figure 8: Bullets positioned together with the surrounding paragraphs.*

#### Ordered lists

Now you need to consider the same issue as applied to ordered lists. They are trickier since the numeric markers are aligned according to the list item with the largest number. For example, if you have 10 list items, decimals will be positioned to allow for the two-digit "10" item, as seen in Figure 9:

![Screenshot of ten-item list, with the markers indented to allow for the 10.](//static.webplatform.org/2/2c/ol-inden.gif)

*Figure 9: The numeric marker for items 1-9 have preceding padding so they right-align with item 10.*

So, there really isn't a way to make this consistently left-aligned to the same position as the surrounding text; unless you set the list to use `list-style-type: decimal-leading-zero;`, which will hide the issue, as seen in Figure 10:

![Screenshot of leading zeros allowing numbers to left-align consistently.](//static.webplatform.org/b/bf/ol-indeo.gif)

*Figure 10: The leading zeros fill in the space for items 1-9.*

It is more common to simply live with the difference in spacing. It does however mean that the markers of your ordered and unordered lists can't easily be consistently left-aligned. You can only line up the *text* of your lists:

    ul, ol {
      margin-left: 0;
      padding-left: 0;
    }

    li {
      margin-left: 2em;
    }

You need *at least*2em of left margin to accomodate both ordered and unordered lists. In Figure 11, note the way the text of the items lines up in both lists:

![Screenshot of lists set to have text consistently left-aligned.](//static.webplatform.org/c/ce/list-ing.gif)

*Figure 11: The text lines up in both ordered and unordered lists.*

#### So, what to do?

You basically have three choices:

1.  Live with the default positioning of lists and their markers
2.  Explicitly line up the text of your lists
3.  Set a different style for `ul` and `ol`.

There is no "right" or "wrong" approach and it is quite common to simply leave things to the default settings for lists in general content.

### Using list-style-position

If you want the text of multi-line list items to wrap below the list marker, you will need to set the `list-style-position` property to `inside`, which produces the result seen in Figure 12:

![Screenshot of unordered list with text wrapping below bullets.](//static.webplatform.org/c/c8/inside-l.gif)

*Figure 12: List position "inside" causes the text to wrap below the marker instead of in line with the indented text.*

Inside positioned markers is not an especially popular style. By default `list-style-position` is set to `outside`, which produces the results discussed elsewhere in this article.

### What about definition lists?

In general, definition lists don't require a huge amount of attention, except to set a `dt` style (commonly bold text) and control the indentation of the definitions:

    dt {
      font-weight: bold;
    }

    dd {
      margin-left: 2em;
    }

This sets up a clear and easy style for definition lists, as seen in Figure 13:

![Screenshot of a definition list with bold terms and indented definitions.](//static.webplatform.org/4/4d/definiti.gif)

*Figure 13: A simply styled definition list.*

Although definition lists can be rearranged with floats and positioning, they are quirky and generally it's better to keep things simple. They are useful enough as they are, just with a little help to make the definition terms stand out more; and to get the definitions to indent nicely.

### Nested lists

In the [HTML Lists](/guides/html_lists) article you learned about nesting lists. When you create your CSS you should be careful to maintain clear design cues to show the relationship between a nested list and the list that contains it. By far the most common way to do this is by indenting the nested list items—it is in fact the default setting across the browsers.

If you set up your own list indentation, your base setting will simply be multiplied. For example, consider this CSS:

    ul, ol {
      margin-left: 0;
      padding-left: 0;
    }

    li {
      margin-left: 2em;
    }

Each subsequent child list item in the chain inherits the `margin` value from its parent list item, in addition to having another 2em of its own added on top. So a top level list item (one that doesn't have a list item as a parent element) will have a left margin of 2em, then a child list item of the first list item will inherit 2em from its parent, and then have another 2em added on to it, for a total of 4em … and so on.

### Horizontal lists

One of the most common changes required to work with a list is to produce a horizontal list—that is, to make the items appear next to each other instead of one after the other. This is a common trick for site navigation. Let's use an example from the navigation menus article (see Figure 14):

![Screenshot of a simple list with bullets](//static.webplatform.org/5/5d/simple-n.gif)

*Figure 14: A simple list.*

Let's convert this to a horizontal list, as shown in Figure 15:

![Screenshot of a list with the items appearing next to each other](//static.webplatform.org/b/b4/simple-o.gif)

*Figure 15: A simple horizontal list.*

To achieve this, we need to do three things to our list:

1.  Remove the `margin` and `padding` from the `<ul>`
2.  Set the list items to `display: inline;`
3.  Give the list items some spacing to the right, to avoid having them run together

In the example the list has the ID "mainmenu" so we'll use that as a contextual selector, to make sure we only change the list we intend to change. The CSS is:

    #mainmenu {
      margin: 0;
      padding: 0;
    }

    #mainmenu li {
      display: inline;
      padding: 0 1em 0 0;
    }

In this simple example, setting the list items to `display: inline;` is enough; be aware that using `float: left;` will also achieve a similar look. You will learn more about [floats](/tutorials/floats_and_clearing) elsewhere in this tutorial group.

### Faux columns

Earlier on we created a list of RSS feeds. Now let's imagine that list has been placed in a sidebar on your site. The designer wants the list to appear in two columns, with a border around the whole group as seen in Figure 16.

![Screenshot of a list in two columns.](//static.webplatform.org/1/16/columns-.gif)

*Figure 16: A list of feeds in two columns, with an RSS icon for each bullet.*

Let's assume the list is inside a `<div>` which sets the width and border. The basic list would look something like Figure 17:

![Screenshot of basic list](//static.webplatform.org/b/be/columns0.gif)

*Figure 17: The unstyled list inside the border.*

To achieve the faux columns effect, add the RSS icon as demonstrated earlier; then add 5px margin to the top, right and left:

    .rss {
      margin: 5px 5px 0 5px;
      padding: 0;
    }

    .rss li {
      list-style-type: none;
      background: #fff url("icon-rssfeed.gif") 0 3px no-repeat;
      padding: 0 0 5px 15px;
      display:-moz-inline-box;
    }

Note that `display:-moz-inline-box;` is added to get the example to display correctly in Firefox 2.

We don't need to add bottom margin as the last list item will add the correct spacing with its padding, as seen in Figure 18:

![Screenshot of list with the correct spacing and icon.](//static.webplatform.org/6/68/columns1.gif)

*Figure 18: Halfway there—we now have correct spacing and icon bullets.*

Now set the list items to `display: inline-block;` and set their width to `40%` and right margin to `2%` (you could also use pixel widths). You also need to explicitly set the `<ul>` to have `100%` width, to ensure that the list wraps and sizes correctly:

    .rss {
      margin: 5px 5px 0 5px;
      padding: 0;
      width: 100%;
    }

    .rss li {
      display: inline-block;
      width: 40%;
      margin: 0 2% 0 0;
      list-style-type: none;
      background: #fff url("icon-rssfeed.gif") 0 3px no-repeat;
      padding: 0 0 5px 15px;
      display:-moz-inline-box;
    }

In most browsers this will be enough to create the column effect, but you will need to explicitly set IE to float the list items to the left. Let's use a conditional style for all versions up to IE7 (since we don't yet know what future versions will do):

    <!--[if lte IE 7]>
      <style type="text/css">
        .rss li {
          float: left;
        }
      </style>
    <![endif]-->

We now have the desired two column effect, as seen in Figure 19:

![Screenshot of a list in two columns.](//static.webplatform.org/1/16/columns-.gif)

*Figure 19: The completed list.*

#### Legacy browsers

If you are required to produce this design for older browsers that don't support inline-block, then you will need to float the list items to the left in all browsers and use a clearing fix like the one described in the article [Clearing a float container without source markup](http://www.positioniseverything.net/easyclearing.html). Thankfully the latest round of browser releases has made `inline-block` a viable display property, so unless you have a very large browser share for older browsers such as Firefox 2 you should be able to use the `inline-block` method.

### Lists conclusion

We've now covered a core set of styling choices and methods for lists. You can build on these examples and combine them to create a large number of designs. Since lists are very commonly combined with links, let's move on to links.

## Styling Links

Styling links can be a bit of an art form. There are many different requirements at play and it can be hard to accommodate them all, while still creating an aesthetically pleasing result. That said, it is quite possible so long as you keep some simple rules in mind:

-   understand the different link states
-   do not stray too far from user expectations
-   use colours carefully

If you follow those rules you should produce links that are clear and easy to use.

### Understanding link states

Before you can style links, you need to understand the different **link states**. There are five states in total: unvisited/default, visited, focus, hover and active.

-   `:unvisited` — The default state of a link when it has not been activated or visited previously.
-   `:visited` — The state of a link the user has already visited.
-   `:focus` — Applies while the link has focus—for example while a keyboard user's cursor is on that link.
-   `hover` — Applies while a user is "hovering" over the link with a pointer like a mouse, but has not yet clicked the link.
-   `active` — Applies while the user activates the link—literally *during*the time they are clicking it. In some browsers this style also applies when the link has been opened in another window or tab.

Note: IE does not currently support the focus state, and just uses `active` in place of `focus`.

You should always specify CSS for every one of these states. Each one conveys information to the user about the fact they are interacting with a link. If in doubt about `focus`, `hover` and `active` you can simply style `focus` and `hover` in the same way as their functions are similar enough that the same link style should not actively cause confusion. You can then add some simple variation for `active`, for example setting the text to italics. At a pinch you can style all three the same way.

Note that these states are not all mutually exclusive (although it is not really possible for a link to be unvisited and visited at the same time)—it is however perfectly possible for a link to be hovered, active and visited at the same time.

### How browser evolution set expectations

To better understand some common user expectations about links, it helps to know a little web history.

You may hear people refer to the "Netscape defaults" for links; or say that links should always be blue and purple. This harks back to the very early days of the web, when browsers set the colours for content and authors didn't have much control over the rendering of their pages.

Text was black, the background was grey, and all links were underlined. The unvisited links were blue, visited links were purple, and active links were red — and that was about it. See Figure 20 for an illustration of this.

![Screenshot of the Mosaic/Navigator startup page, explaining hyperlinks.](//static.webplatform.org/d/de/links-mo.gif)

*Figure 20: A screenshot of Mosaic.*

While this did get a bit monotonous it was *consistent* — and **it set the baseline for user expectations**. In particular, to this day users expect underlined text to be a link. They may not expect all links to have underlines, but they definitely expect underlined text to be clickable. It is best not to clash with that expectation.

Some sites still use blue and purple links; and those link colours are still the default for unstyled content in most browsers. While you can always go retro and stick with this colour set, users are generally quite comfortable with other options—within certain boundaries.

### User expectations

There are some general rules for user expectations regarding links:

-   Users expect links to **look different** from other text which is not a link
-   Users expect links to **react** when they hover or focus on the link
-   Users expect links to **change** after they have visited that link
-   Users like **consistency** in link styles of the same functionality so they know what to click
-   Users expect underlined text to be a link—so don't use underlines for anything else

You should always cater to these basic rules, as they will help your users quickly identify and use links. You want to create styles that don't make people stop and think "which bits are links"?

These expectations translate to some simple coding rules:

-   set styles for all link states
-   only use underlining for links

### Use colour carefully

When you are styling links, be careful not to rely entirely on colour to distinguish between link states. Not everyone can see colour the same (eg people with colour blindness), so you should use colour *and* styles like different underlines, icons or reversed colours.

You should also check that your colour choices have enough contrast—this is really easy using tools like the [Colour Contrast Analyser (for both PC and Mac)](http://www.paciellogroup.com/resources/contrastanalyser/) or the [Web Accessibility Toolbar for Opera](http://www.paciellogroup.com/resources/wat/) (both from the Paciello Group).

The Colour Contrast Analyser (see Figure 21) allows you to use a colour picker to select the foreground and background colours on screen, then receive a simple evaluation of their contrast:

![The CCA tool showing a test of heading colour.](//static.webplatform.org/7/78/cca-in-u.gif)

*Figure 21: Screenshot of the Colour Contrast Analyser in use.*

If all four results show a pass, the colour combination is ok. Remember to check all link states. You may need to enter some of them manually in the "hex" field to check focus, hover and active.

### Getting down to business: the CSS

Now that you understand some ground rules for links, let's get into some code—this section details all the CSS you'll need to sucessfully style links.

#### Styling link states in the right order

First off, be aware that if you do not place your links styles in the right order in your stylesheet, the settings will override each other and the link states won't work. Your link styles must always be in the following order:

1.  `link`
2.  `visited`
3.  `focus`
4.  `hover`
5.  `active`

A common mnemonic for remembering this is "Lord Vader's Former Handle, Anakin". If you're not a Star Wars fan, I'm afraid you'll just have to remember it the hard way, or copy and paste the code block below!

Also popular is the mnemonic "LoVe Fears HAte", with "Fears" standing for "Focus".

The different link states are styled using their "pseudo classes"—`:link`, `:visited`, `:focus`, `:hover`, `:active` —which you append to the link element selector, `a`. So your starting CSS should look like this:

    a:link {}
    a:visited {}
    a:focus {}
    a:hover {}
    a:active {}

If you want to set a CSS rule for all links in all states, you can style `a` directly. Just remember to place the generic rule first, to preserve the order:

    a {}
    a:link {}
    a:visited {}
    a:focus {}
    a:hover {}
    a:active {}

This is useful if you are planning to replace the default underline with a bottom border, which is a common way to gain better visual control of the style.

#### Controlling defaults

By default, most browsers set all links to have an underline and focus state links to have an outline, as illustrated in Figure 22:

![The default focus style for Opera 9, Firefox 2 and IE7](//static.webplatform.org/f/ff/browser-.gif)

*Figure 22: Left to right: the default focus styles for Opera 9, Firefox 2 and IE7.*

If you are replacing these styles with something else, you can change or disable these defaults.

##### Underlining

Underlining is set using the [text-decoration](http://www.w3.org/TR/REC-CSS2/text.html#lining-striking-props) property:

    a {
      text-decoration: underline;
    }

You can disable the underline by setting the property to `none`:

    a {
      text-decoration: none;
    }

Even if you are conserving the underline style, you may find it easier to disable `text-decoration` and use `border-bottom` to set a faux underline. We will go through this in the example below.

##### Outline

The focus outline is controlled by the [outline](http://www.w3.org/TR/REC-CSS2/ui.html#dynamic-outlines) property. Outline is much the same as border, but it does not take up space or cause the page to re-flow when it appears (note that it is not supported in IE7 and below either). The easiest way to control outline is with the shorthand property:

    a:focus {
      outline: thick solid #000;
    }

This example would be rendered something like Figure 23:

![A link with a thick black border.](//static.webplatform.org/a/a4/thick-so.gif)

*Figure 23: example rendering of a thick black outline.*

If you are in doubt about what to do with the outline, simply leave the outline to the browser default.

### Example: recreating the Netscape defaults

As an easy example of link styles, let's recreate the Netscape defaults of blue, purple and red. We'll keep the underline, but extend the active state to use italics. We'll increase the text size for the sake of the example and set the page to use a white background:

    body {
      background: #fff;
      color: #000;
      font-size: 2em;
    }

    a {
      text-decoration: underline;
    }

    a:link {
      color: #0000CC;
    }

    a:visited {
      color: #6D006D;
    }

    a:focus {
      color: #CC0000;
    }

    a:hover {
      color: #CC0000;
    }

    a:active {
      color: #CC0000;
      font-style: italic;
    }

This should produce something like Figure 24:

![Example rendering of the styles set above](//static.webplatform.org/9/92/lvfha-un.gif)

*Figure 24: recreating the Netscape defaults.*

#### Faux underlines using border-bottom

Many designers have observed that underlining is a bit thick and cuts through descenders of lowercase type—that is, the line goes through the bottom of g, j, p, q and y. This is illustrated in figure 25:

![The word pygmy showing the underline cutting through the text](//static.webplatform.org/d/d5/pygmy-un.gif)

*Figure 25: The underline cuts through lowercase type descenders.*

Let's assume that the person designing your site agrees, and would like the underline to be thinner and not touch the text. To carry out this common request, we'll use a border instead of an underline so it looks like Figure 26:

![The word pygmy showing a faux underline border, which does not cut through the text](//static.webplatform.org/2/22/pygmy-bo.gif)

*Figure 26: Using a border instead of an underline gives nicer results.*

First, disable the underline for all link states, then set a bottom-border to match the link colour for each state:

    body {
      background: #fff;
      color: #000;
      font-size: 2em;
      line-height: 2em;
    }

    a {
      text-decoration: none;
    }

    a:link {
      color: #00c;
      border-bottom: 1px solid #00c;
    }

    a:visited {
      color: #6D006D;
      border-bottom: 1px solid #6D006D;
    }

    a:focus {
      color: #c00;
      border-bottom: 1px solid #c00;
    }

    a:hover {
      color: #c00;
      border-bottom: 1px solid #c00;
    }

    a:active {
      color: #c00;
      border-bottom: 1px solid #c00;
      font-style: italic;
    }

This should produce something like Figure 27:

![Example rendering of the styles set above](//static.webplatform.org/8/81/Lvfha-bo.gif)

*Figure 27: The faux-underline in action.*

If you do use the faux border method, be careful that you have sufficient `line-height` set to avoid the underline clashing with the next row of text.

#### Styles that don't rely on colour

Since the example so far relies purely on colour to distinguish four of the five link states, we should take the next step and change the bottom border for visited, focus and hover. Let's give visited links a dotted border, and hovered and focused links a dashed border:

    body {
      background: #fff;
      color: #000;
      font-size: 2em;
    }

    a {
      text-decoration: none;
    }

    a:link {
      color: #00c;
      border-bottom: 1px solid #00c;
    }

    a:visited {
      color: #6D006D;
      border-bottom: 1px dotted #6D006D;
    }

    a:focus {
      color: #c00;
      border-bottom: 1px dashed #c00;
    }

    a:hover {
      color: #c00;
      border-bottom: 1px dashed #c00;
    }

    a:active {
      color: #c00;
      border-bottom: 1px solid #c00;
      font-style: italic;
    }

This should produce something like Figure 28:

![Example rendering showing how the borders differentiate the different link states](//static.webplatform.org/4/46/Lvfha-mu.gif)

*Figure 28: Changing the border style for each link state.*

Accepting focus and hover as equivalent styled states, this method means the link states are distinguished with more than colour. Even if you were to view these links in black and white, you could identify the different link states, as shown in Figure 29:

![The same example all in black, to emphasise the border differences](//static.webplatform.org/d/da/Lvfha-mv.gif)

*Figure 29: The link states are now distinguishable even in black and white.*

### Icons on links

Some sites use icons and symbols to add information about their links. For example, some sites use an arrow to indicate that a link goes to an external site; or they use a tick to show the link has been visited.

These effects are simple to achieve with background images, as shown in Figure 30:

![Example rendering of links with icons](//static.webplatform.org/f/f1/Links-wi.gif)

*Figure 30: An example of links with distinguishing icons.*

To add an arrow icon to external links you could add the class "external" to the link tag:

    <a href="http://example.com/" class="external">external link</a>

Then in your stylesheet, set a background image for that class—remembering to add padding to accommodate the image:

    a.external {
      background: #fff url("icon-external.gif") center right no-repeat;
      padding-right: 30px;
    }

This example would apply the icon to all instances of visited links, in all states. If you wanted to restrict the icon just to *unvisited* external links, you can combine classes and the link state pseudo classes in your selector:

    a.external:link {
      background: #fff url("icon-external.gif") center right no-repeat;
      padding-right: 30px;
    }

Combining classes and states opens up a wide range of creative possibilities for your links. Remembering to check your colours, your only limitation from this point is creativity.

## Bringing it all together—a simple navigation menu

To illustrate one way to bring lists and links together, the examples zip includes a simple flyout navigation menu, as seen in Figure 31. Flyout menus are a very common navigation system.

![Screenshot of the flyout list example.](//static.webplatform.org/1/1b/Flyout-l.gif)

*Figure 31: Screenshot of the example flyout menu.*

## See also

### External resources

-   [WCAG Samurai Errata for WCAG 1.0](http://www.wcagsamurai.org/errata/errata.html), with specific reference to [Guideline 2. Don’t rely on colour alone](http://www.wcagsamurai.org/errata/errata.html#GL2).
-   [Type and Colour (a chapter from Building Accessible Websites, by Joe Clark)](http://joeclark.org/book/sashay/serialization/Chapter09.html)
-   [Juicy Studio: Highlighting Links](http://juicystudio.com/article/highlighting-links.php)
-   [Max Design—Simple, accessible external links](http://www.maxdesign.com.au/presentation/external/)
-   [Resource Center—Contrast Analyser 2.0 (Paciello Group)](http://www.paciellogroup.com/resources/contrast-analyser.html)
-   [A List Apart: CSS Sprites: Image Slicing’s Kiss of Death](http://alistapart.com/articles/sprites)

### Exercise questions

-   How do you choose between basic list styles, for example square bullets or Roman Numerals on an ordered list?
-   What is an image sprite and why would you use one?
-   Why is colour contrast important and how do you make sure your link colours are using suitable colours?
-   What is the correct order for setting styles on the different link states?
