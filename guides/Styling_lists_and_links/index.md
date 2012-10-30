== Introduction ==
 
Many elements on a webpage are a little bit "forgiving" in terms of design—if they’re not "just right" it doesn’t matter too much. With lists and links it’s a different story—if you don’t get them right, you can cause some serious problems for people trying to use your website.
 
Links in particular have some key style requirements and user expectations. Poorly styled links can ruin the user experience on a website, as people have to stop and think about where to click. In the worst case, a user might not even be able to tell which items on the page are actually links.
 
In this [http://www.w3.org/wiki/Web_Standards_Curriculum Web Standards Curriculum] article we’ll look at the core skills you need to create robust list and link styles. We’ll also discuss some ways to avoid key pitfalls of these elements and produce a final result that will work across different browsers, and be accessible to users with disabilities.
 
There are a number of examples used in this article, so you can [http://dev.opera.com/articles/view/32-styling-lists-and-links/styling-lists-and-links-examples.zip download the lists and links example files] to follow along with them.

== Styling Lists ==
 
First, I’ll take you through the basics of styling lists with CSS, before then moving on to look at some slightly more complicated techniques.
 
=== Basic bullets and numbers ===
 
The fundamental thing to consider when creating a list style is what form of bullet or numbering you want to use. You might also choose to remove the bullets and numbers completely. As you learned in the [http://www.w3.org/wiki/HTML_lists HTML Lists article], there are many options available, set using the <code>list-style-type</code> property.
 
For example, to set all unordered lists on your site to use square bullets, use this CSS:
 
<pre>ul li {
  list-style-type: square;
}</pre>
 
Which will produce something like Figure 1:
 
[[Image:square-b.gif|Screenshot of a list with square bullets]]
 
Figure 1: Unordered list with square bullets.
 
Some common list types are shown in Figure 2:
 
[[Image:referenc.gif|Screenshot of some common list types.]]
 
Figure 2: Common list styles.
 
The [http://dev.opera.com/articles/view/32-styling-lists-and-links/styling-lists-example-basics.html basic list choices example page] shows some more options.
 
Note that the bullets and numbers will be rendered using the <code>color</code> which is set for or inherited by the <code>li</code>. If you need the bullet to be a different colour from the text, you will need to use an image instead, or work around the issue using other elements within the list items (this may be easy if all the items are links, for example).

=== Custom bullets using images ===
 
The standard set of bullets are enough for basic content, however it is a common design request to replace them with a custom image.
 
The CSS specification does include the <code>list-style-image</code> property for adding a custom list image. However, the property has limited positioning options for the background image, and in some circumstances doesn’t work at all in IE. So it has become a far more common practice to simply set a background image on the list items.
 
Let’s imagine you have a list of RSS feeds and you want to change the bullet to the standard orange RSS icon. We’ll give the list the class "rss" to differentiate it from other lists:
 
<pre>&lt;ul class="rss"&gt;
  &lt;li&gt;&lt;a href="http://example.com/rss.xml"&gt;News&lt;/a&gt;&lt;/li&gt;
  &lt;li&gt;&lt;a href="http://example.com/rss.xml"&gt;Sport&lt;/a&gt;&lt;/li&gt;
  &lt;li&gt;&lt;a href="http://example.com/rss.xml"&gt;Weather&lt;/a&gt;&lt;/li&gt;
  &lt;li&gt;&lt;a href="http://example.com/rss.xml"&gt;Business&lt;/a&gt;&lt;/li&gt;
  &lt;li&gt;&lt;a href="http://example.com/rss.xml"&gt;Entertainment&lt;/a&gt;&lt;/li&gt;
  &lt;li&gt;&lt;a href="http://example.com/rss.xml"&gt;Funny News&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;</pre>
 
First we’ll set the list to have no <code>list-style-type</code> and remove the margin and padding. Then, simply add a background image to each list item, some left padding to move the text over to let the image show through, and some bottom padding to space out the list items:
 
<pre>.rss {
  margin: 0;
  padding: 0;
  list-style-type: none;
}

.rss li {
  background: #fff url("icon-rssfeed.gif") 0 3px no-repeat;
  padding: 0 0 5px 15px;
}</pre>
 
This will produce a list with the RSS image instead of bullets, as seen in Figure 3:

[[Image:image-bu.gif|Screenshot of a list with the bullets replaced with images]]
 
Figure 3: The list with image bullets.
 
Bear in mind that the background image is positioned using pixels for a precise placement. Depending on the design you are creating, you might also be able to use <code>%</code>, <code>em</code>s or keywords. Just be careful when your design features content that might cause a list item to wrap over several lines—if you set the background to vertical <code>center</code> or <code>50%</code> it can look quite strange, as shown in Figure 4:
 
[[Image:image-bv.gif|Screenshot showing the way the vertically-centred bullet will sit in the middle of the text, instead of being centred to the first line of text.]]
 
Figure 4: A demonstration of vertically-centred bullet images on a multi-line list item.
 
By setting the image to sit at the top of the list item, you maintain the default bullet behaviour (where the bullet sits on the first line)—see Figure 5:
 
[[Image:image-bw.gif|Screenshot of top-positioned bullet images.]]

Figure 5: A demonstration of top-aligned bullet images on a multi-line list item.
 
=== List margins and padding ===
 
Clever use of margins and padding can make lists look much more polished and professional, but you need to know what you are doing, and also bear in mind that the situation differs between different types of list. In this section I’ll take you through applying sensible margins and padding to the two most common types of list.
 
==== Unordered lists ====
 
One thing you will probably notice quite quickly is that the default style for lists indents them more than the default style for paragraphs—see Figure 6:
 
[[Image:list-ind.gif|Screenshot of default list styles with a larger left indent than paragraphs.]]
 
Figure 6: Default styled lists are indented on the left.
 
If you want your unordered list items to sit at the same left-align point as the rest of your content, you will need to set some styles to control the indentation to your liking. Different browsers require different settings—some need the margin removed, others need the padding removed. So, to reset for all browsers, reset both:
 
<pre>ul {
  margin: 0;
  padding: 0;
}</pre>
 
This may not have the effect you were expecting, as it will get the ''text'' to sit flush left but the bullets will sit outside the text, as shown in Figure 7:
 
[[Image:list-ine.gif|Screenshot of bullets sitting outside the text.]]
 
Figure 7: Bullets are positioned to the left of the text.
 
So, to align the ''bullets'' to the left you can now set a margin on the list items to line things up:
 
<pre>ul {
  margin-left: 0;
  padding-left: 0;
}

ul li {
  margin-left: 1em;
}</pre>
 
...at this point you will still find a pixel-level difference between browsers but the effect is basically as consistent as possible—see Figure 8:
 
[[Image:list-inf.gif|Screenshot of bullets left-aligned closely with paragraphs.]]
 
Figure 8: Bullets positioned together with the surrounding paragraphs.
 
==== Ordered lists ====
 
Now you need to consider the same issue as applied to ordered lists. They are trickier since the numeric markers are aligned according to the list item with the largest number. For example, if you have 10 list items, decimals will be positioned to allow for the two-digit "10" item, as seen in Figure 9:
 
[[Image:ol-inden.gif|Screenshot of ten-item list, with the markers indented to allow for the 10.]]
 
Figure 9: The numeric marker for items 1–9 have preceding padding so they right-align with item 10.
 
So, there really isn’t a way to make this consistently left-aligned to the same position as the surrounding text; unless you set the list to use <code>list-style-type: decimal-leading-zero;</code>, which will hide the issue, as seen in Figure 10:
 
[[Image:ol-indeo.gif|Screenshot of leading zeros allowing numbers to left-align consistently.]]
 
Figure 10: The leading zeros fill in the space for items 1–9.
 
It is more common to simply live with the difference in spacing. It does however mean that the markers of your ordered and unordered lists can’t easily be consistently left-aligned. You can only line up the ''text'' of your lists:
 
<pre>ul, ol {
  margin-left: 0;
  padding-left: 0;
}

li {
  margin-left: 2em;
}</pre>
 
You need ''at least ''2em of left margin to accomodate both ordered and unordered lists. In Figure 11, note the way the text of the items lines up in both lists:
 
[[Image:list-ing.gif|Screenshot of lists set to have text consistently left-aligned.]]
 
Figure 11: The text lines up in both ordered and unordered lists.
 
==== So, what to do? ====
 
You basically have three choices:
 
# Live with the default positioning of lists and their markers
# Explicitly line up the text of your lists
# Set a different style for <code>ul</code> and <code>ol</code>.
 
There is no "right" or "wrong" approach and it is quite common to simply leave things to the default settings for lists in general content.
 
=== Using list-style-position ===
 
If you want the text of multi-line list items to wrap below the list marker, you will need to set the <code>list-style-position</code> property to <code>inside</code>, which produces the result seen in Figure 12:
 
[[Image:inside-l.gif|Screenshot of unordered list with text wrapping below bullets.]]
 
Figure 12: List position "inside" causes the text to wrap below the marker instead of in line with the indented text.
 
Inside positioned markers is not an especially popular style. By default <code>list-style-position</code> is set to <code>outside</code>, which produces the results discussed elsewhere in this article.
 
=== What about definition lists? ===
 
In general, definition lists don’t require a huge amount of attention, except to set a <code>dt</code> style (commonly bold text) and control the indentation of the definitions:
 
<pre>dt {
  font-weight: bold;
}

dd {
  margin-left: 2em;
}</pre>
 
This sets up a clear and easy style for definition lists, as seen in Figure 13:
 
[[Image:definiti.gif|Screenshot of a definition list with bold terms and indented definitions.]]
 
Figure 13: A simply styled definition list.
 
Although definition lists can be rearranged with floats and positioning, they are quirky and generally it’s better to keep things simple. They are useful enough as they are, just with a little help to make the definition terms stand out more; and to get the definitions to indent nicely.
 
=== Nested lists ===
 
In the [http://www.w3.org/wiki/HTML_lists HTML Lists article] you learned about nesting lists. When you create your CSS you should be careful to maintain clear design cues to show the relationship between a nested list and the list that contains it. By far the most common way to do this is by indenting the nested list items—it is in fact the default setting across the browsers.
 
If you set up your own list indentation, your base setting will simply be multiplied. For example, consider this CSS:
 
<pre>ul, ol {
  margin-left: 0;
  padding-left: 0;
}

li {
  margin-left: 2em;
}</pre>
 
Each subsequent child list item in the chain inherits the <code>margin</code> value from its parent list item, in addition to having another 2em of its own added on top. So a top level list item (one that doesn’t have a list item as a parent element) will have a left margin of 2em, then a child list item of the first list item will inherit 2em from its parent, and then have another 2em added on to it, for a total of 4em … and so on.

=== Horizontal lists ===
 
One of the most common changes required to work with a list is to produce a horizontal list—that is, to make the items appear next to each other instead of one after the other. This is a common trick for site navigation. Let’s use an example from the navigation menus article (see Figure 14):
 
[[Image:simple-n.gif|Screenshot of a simple list with bullets]]
 
Figure 14: A simple list.
 
Let’s convert this to a horizontal list, as shown in Figure 15:
 
[[Image:simple-o.gif|Screenshot of a list with the items appearing next to each other]]
 
Figure 15: A simple horizontal list.
 
To achieve this, we need to do three things to our list:
 
# Remove the <code>margin</code> and <code>padding</code> from the <code>&lt;ul&gt;</code>
# Set the list items to <code>display: inline;</code>
# Give the list items some spacing to the right, to avoid having them run together
 
In the example the list has the ID "mainmenu" so we’ll use that as a contextual selector, to make sure we only change the list we intend to change. The CSS is:
 
<pre>#mainmenu {
  margin: 0;
  padding: 0;
}

#mainmenu li {
  display: inline;
  padding: 0 1em 0 0;
}</pre>
 
In this simple example, setting the list items to <code>display: inline;</code> is enough; be aware that using <code>float: left;</code> will also achieve a similar look. You will [http://dev.opera.com/articles/view/35-floats-and-clearing/ learn more about floats] later on in the course.

=== Faux columns ===
 
Earlier on we created a list of RSS feeds. Now let’s imagine that list has been placed in a sidebar on your site. The designer wants the list to appear in two columns, with a border around the whole group as seen in Figure 16 (check out [http://dev.opera.com/articles/view/32-styling-lists-and-links/styling-lists-example-columns.html styling-lists-example-columns.html] for the faux-columns example.)
 
[[Image:columns-.gif|Screenshot of a list in two columns.]]
 
Figure 16: A list of feeds in two columns, with an RSS icon for each bullet.
 
Let’s assume the list is inside a <code>&lt;div&gt;</code> which sets the width and border. The basic list would look something like Figure 17 (see [http://dev.opera.com/articles/view/32-styling-lists-and-links/styling-lists-example-image-bullet.html styling-lists-example-image-bullet.html] for the basic starting list):
 
[[Image:columns0.gif|Screenshot of basic list]]

Figure 17: The unstyled list inside the border.
 
To achieve the faux columns effect, add the RSS icon as demonstrated earlier; then add 5px margin to the top, right and left:
 
<pre>.rss {
  margin: 5px 5px 0 5px;
  padding: 0;
}

.rss li {
  list-style-type: none;
  background: #fff url("icon-rssfeed.gif") 0 3px no-repeat;
  padding: 0 0 5px 15px;
  display:-moz-inline-box;
}</pre>
 
Note that <code>display:-moz-inline-box;</code> is added to get the example to display correctly in Firefox 2.
 
We don’t need to add bottom margin as the last list item will add the correct spacing with its padding, as seen in Figure 18:
 
[[Image:columns1.gif|Screenshot of list with the correct spacing and icon.]]
 
Figure 18: Halfway there—we now have correct spacing and icon bullets.
 
Now set the list items to <code>display: inline-block;</code> and set their width to <code>40%</code> and right margin to <code>2%</code> (you could also use pixel widths). You also need to explicitly set the <code>&lt;ul&gt;</code> to have <code>100%</code> width, to ensure that the list wraps and sizes correctly:
 
<pre>.rss {
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
}</pre>
 
In most browsers this will be enough to create the column effect, but you will need to explicitly set IE to float the list items to the left. Let’s use a conditional style for all versions up to IE7 (since we don’t yet know what future versions will do):
 
<pre>&lt;!--[if lte IE 7]&gt;
  &lt;style type="text/css"&gt;
    .rss li {
      float: left;
    }
  &lt;/style&gt;
&lt;![endif]--&gt;</pre>
 
We now have the desired two column effect, as seen in Figure 19:
 
[[Image:columns-.gif|Screenshot of a list in two columns.]]
 
Figure 19: The completed list.
 
==== Legacy browsers ====
 
If you are required to produce this design for older browsers that don’t support inline-block, then you will need to float the list items to the left in all browsers and use a clearing fix like the one described in the article [http://www.positioniseverything.net/easyclearing.html Clearing a float container without source markup]. Thankfully the latest round of browser releases have made <code>inline-block</code> a viable display property, so unless you have a very large browser share for older browsers such as Firefox 2 you should be able to use the <code>inline-block</code> method.

=== Lists conclusion ===
 
We’ve now covered a core set of styling choices and methods for lists. You can build on these examples and combine them to create a large number of designs. Since lists are very commonly combined with links, let’s move on to links.
 
== Styling Links ==
 
Styling links can be a bit of an art form. There are many different requirements at play and it can be hard to accommodate them all, while still creating an aesthetically pleasing result. That said, it is quite possible so long as you keep some simple rules in mind:
 
* understand the different link states
* do not stray too far from user expectations
* use colours carefully
 
If you follow those rules you should produce links that are clear and easy to use.
 
=== Understanding link states ===
 
Before you can style links, you need to understand the different '''link states'''. There are five states in total: unvisited/default, visited, focus, hover and active.

;unvisited
:The default state of a link when it has not been activated or visited previously.
;visited
:The state of a link the user has already visited.
;focus
:Applies while the link has focus—for example while a keyboard user’s cursor is on that link. Note: IE  does not currently support the focus state, and just uses <code>active</code> in place of <code>focus</code>.
;hover
:Applies while a user is "hovering" over the link with a pointer like a mouse, but has not yet clicked the link.
;active
:Applies while the user activates the link—literally ''during ''the time they are clicking it. In some browsers this style also applies when the link has been opened in another window or tab.

You should always specify CSS for every one of these states. Each one conveys information to the user about the fact they are interacting with a link. If in doubt about <code>focus</code>, <code>hover</code> and <code>active</code> you can simply style <code>focus</code> and <code>hover</code> in the same way as their functions are similar enough that the same link style should not actively cause confusion. You can then add some simple variation for <code>active</code>, for example setting the text to italics. At a pinch you can style all three the same way.
 
Note that these states are not all mutually exclusive (although it is not really possible for a link to be unvisited and visited at the same time)—it is however perfectly possible for a link to be hovered, active and visited at the same time.
 
=== How browser evolution set expectations ===
 
To better understand some common user expectations about links, it helps to know a little web history.
 
You may hear people refer to the "Netscape defaults" for links; or say that links should always be blue and purple. This harks back to the very early days of the web, when browsers set the colours for content and authors didn't have much control over the rendering of their pages.
 
Text was black; the background was grey; and all links were underlined. The unvisited links were blue, visited links were purple and active links were red…and that was about it. See Figure 20 for an illustration of this.

[[Image:links-mo.gif|Screenshot of the Mosaic/Navigator startup page, explaining hyperlinks.]]
 
Figure 20: A screenshot of Mosaic.
 
While this did get a bit monotonous it was ''consistent''—and '''it set the baseline for user expectations'''. In particular, to this day users expect underlined text to be a link. They may not expect all links to have underlines, but they definitely expect underlined text to be clickable. It is best not to clash with that expectation.
 
Some sites still use blue and purple links; and those link colours are still the default for unstyled content in most browsers. While you can always go retro and stick with this colour set, users are generally quite comfortable with other options—within certain boundaries.
 
=== User expectations ===
 
There are some general rules for user expectations regarding links:
 
* Users expect links to '''look different ''' from other text which is not a link
* Users expect links to '''react''' when they hover or focus on the link
* Users expect links to '''change''' after they have visited that link
* Users like '''consistency''' in link styles of the same functionality so they know what to click
* Users expect underlined text to be a link—so don’t use underlines for anything else
 
You should always cater to these basic rules, as they will help your users quickly identify and use links. You want to create styles that don’t make people stop and think "which bits are links"?!
 
These expectations translate to some simple coding rules:
 
* set styles for all link states
* only use underlining for links
 
=== Use colour carefully ===
 
When you are styling links, be careful not to rely entirely on colour to distinguish between link states. Not everyone can see colour the same (eg people with colour blindness), so you should use colour ''and'' styles like different underlines, icons or reversed colours.
 
You should also check that your colour choices have enough contrast—this is really easy using tools like the [http://www.paciellogroup.com/resources/contrast-analyser.html Colour Contrast Analyser (for both PC and Mac)] or the [http://www.paciellogroup.com/resources/wat-about.html Web Accessibility Toolbar for Opera] (both from the Paciello Group).
 
The Colour Contrast Analyser (see Figure 20) allows you to use a colour picker to select the foreground and background colours on screen, then receive a simple evaluation of their contrast:
 
[[Image:cca-in-u.gif|The CCA tool showing a test of heading colour.]]
 
Figure 21: Screenshot of the Colour Contrast Analyser in use.
 
If all four results show a pass, the colour combination is ok. Remember to check all link states. You may need to enter some of them manually in the "hex" field to check focus, hover and active.

=== Getting down to business: the CSS ===
 
Now that you understand some ground rules for links, let’s get into some code—this section details all the CSS you’ll need to sucessfully style links.
 
==== Styling link states in the right order ====
 
First off, be aware that if you do not place your links styles in the right order in your stylesheet, the settings will override each other and the link states won’t work. Your link styles must always be in the following order:
 
# <code>link</code>
# <code>visited</code>
# <code>focus</code>
# <code>hover</code>
# <code>active</code>
 
A common mnemonic for remembering this is "Lord Vader’s Former Handle, Anakin". If you’re not a Star Wars fan, I’m afraid you’ll just have to remember it the hard way, or copy and paste the code block below!
 
Also popular is the mnemonic "LoVe Fears HAte", with "Fears" standing for "Focus".

The different link states are styled using their "pseudo classes"—<code>:link</code>, <code>:visited</code>, <code>:focus</code>, <code>:hover</code>, <code>:active</code> —which you append to the link element selector, <code>a</code>. So your starting CSS should look like this:
 
<pre>a:link {}
a:visited {}
a:focus {}
a:hover {}
a:active {}</pre>
 
If you want to set a CSS rule for all links in all states, you can style <code>a</code> directly. Just remember to place the generic rule first, to preserve the order:
 
<pre>a {}
a:link {}
a:visited {}
a:focus {}
a:hover {}
a:active {}</pre>
 
This is useful if you are planning to replace the default underline with a bottom border, which is a common way to gain better visual control of the style.
 
==== Controlling defaults ====
 
By default, most browsers set all links to have an underline and focus state links to have an outline, as illustrated in Figure 22:
 
[[Image:browser-.gif|The default focus style for Opera 9, Firefox 2 and IE7]]

Figure 22: Left to right: the default focus styles for Opera 9, Firefox 2 and IE7.
 
If you are replacing these styles with something else, you can change or disable these defaults.
 
===== Underlining =====
 
Underlining is set using the [http://www.w3.org/TR/REC-CSS2/text.html#lining-striking-props text-decoration] property:
 
<pre>a {
  text-decoration: underline;
}</pre>
 
You can disable the underline by setting the property to <code>none</code>:

<pre>a {
  text-decoration: none;
}</pre>
 
Even if you are conserving the underline style, you may find it easier to disable <code>text-decoration</code> and use <code>border-bottom</code> to set a faux underline. We will go through this in the example below.

===== Outline =====
 
The focus outline is controlled by the [http://www.w3.org/TR/REC-CSS2/ui.html#dynamic-outlines outline] property. Outline is much the same as border, but it does not take up space or cause the page to re-flow when it appears (note that it is not supported in IE7 and below either). The easiest way to control outline is with the shorthand property:

<pre>a:focus {
  outline: thick solid #000;
}</pre>
 
This example would be rendered something like Figure 23:
 
[[Image:thick-so.gif|A link with a thick black border.]]
 
Figure 23: example rendering of a thick black outline.
 
If you are in doubt about what to do with the outline, simply leave the outline to the browser default.

=== Example: recreating the Netscape defaults ===
 
As an easy example of link styles, let’s recreate the Netscape defaults of blue, purple and red. We’ll keep the underline, but extend the active state to use italics. We’ll increase the text size for the sake of the example and set the page to use a white background:
 
<pre>body {
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
}</pre>
 
This should produce something like Figure 24:
 
[[Image:lvfha-un.gif|Example rendering of the styles set above]]
 
Figure 24: recreating the Netscape defaults.
 
==== Faux underlines using border-bottom ====
 
Many designers have observed that underlining is a bit thick and cuts through descenders of lowercase type—that is, the line goes through the bottom of g, j, p, q and y. This is illustrated in figure 25:
 
[[Image:pygmy-un.gif|The word pygmy showing the underline cutting through the text]]
 
Figure 25: The underline cuts through lowercase type descenders.
 
Let’s assume that the person designing your site agrees, and would like the underline to be thinner and not touch the text. To carry out this common request, we’ll use a border instead of an underline so it looks like Figure 26:
 
[[Image:pygmy-bo.gif|The word pygmy showing a faux underline border, which does not cut through the text]]

Figure 26: Using a border instead of an underline gives nicer results.
 
First, disable the underline for all link states, then set a bottom-border to match the link colour for each state:
 
<pre>body {
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
}</pre>
 
This should produce something like Figure 27:
 
[[Image:lvfha-bo.gif|Example rendering of the styles set above]]
 
Figure 27: The faux-underline in action.
 
If you do use the faux border method, be careful that you have sufficient <code>line-height</code> set to avoid the underline clashing with the next row of text.
 
==== Styles that don’t rely on colour ====
 
Since the example so far relies purely on colour to distinguish four of the five link states, we should take the next step and change the bottom border for visited, focus and hover. Let’s give visited links a dotted border, and hovered and focused links a dashed border:
 
<pre>body {
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
}</pre>
 
This should produce something like Figure 28:
 
[[Image:lvfha-mu.gif|Example rendering showing how the borders differentiate the different link states]]
 
Figure 28: Changing the border style for each link state.
 
Accepting focus and hover as equivalent styled states, this method means the link states are distinguished with more than colour. Even if you were to view these links in black and white, you could identify the different link states, as shown in Figure 29:
 
[[Image:lvfha-mv.gif|The same example all in black, to emphasise the border differences]]
 
Figure 29: The link states are now distinguishable even in black and white.
 
=== Icons on links ===
 
Some sites use icons and symbols to add information about their links. For example, some sites use an arrow to indicate that a link goes to an external site; or they use a tick to show the link has been visited.
 
These effects are simple to achieve with background images, as shown in Figure 30:
 
[[Image:links-wi.gif|Example rendering of links with icons]]
 
Figure 30: An example of links with distinguishing icons.
 
To add an arrow icon to external links you could add the class "external" to the link tag:
 
<pre>&lt;a href="http://example.com/" class="external"&gt;external link&lt;/a&gt;</pre>
 
Then in your stylesheet, set a background image for that class—remembering to add padding to accommodate the image:
 
<pre>a.external {
  background: #fff url("icon-external.gif") center right no-repeat;
  padding-right: 30px;
}</pre>
 
This example would apply the icon to all instances of visited links, in all states. If you wanted to restrict the icon just to ''unvisited'' external links, you can combine classes and the link state pseudo classes in your selector:
 
<pre>a.external:link {
  background: #fff url("icon-external.gif") center right no-repeat;
  padding-right: 30px;
}</pre>
 
Combining classes and states opens up a wide range of creative possibilities for your links. Remembering to check your colours, your only limitation from this point is creativity.
 
== Bringing it all together—a simple navigation menu ==
 
To illustrate one way to bring lists and links together, the examples zip includes a [http://devfiles.myopera.com/articles/485/stylinglistsexampleflyout.html simple flyout navigation menu], as seen in Figure 31. Flyout menus are a very common navigation system.
 
[[Image:flyout-l.gif|Screenshot of the flyout list example.]]
 
Figure 31: Screenshot of the example flyout menu.

== Summary ==
 
A good grasp of styling lists and links is essential for web developers, as they are used everywhere. They are routinely combined to create site navigation; while a clear link style is critical for the ease of use of any site. Bad link styles can be seriously confusing for everyone and may even make a site unusable for some people.
 
== Exercise questions ==
 
* How do you choose between basic list styles, for example square bullets or Roman Numerals on an ordered list?
* What is an image sprite and why would you use one?
* Why is colour contrast important and how do you make sure your link colours are using suitable colours?
* What is the correct order for setting styles on the different link states?
 
== Further reading ==
 
* [http://www.wcagsamurai.org/errata/errata.html WCAG Samurai Errata for WCAG 1.0], with specific reference to [http://www.wcagsamurai.org/errata/errata.html#GL2 Guideline 2. Don’t rely on colour alone].
* [http://joeclark.org/book/sashay/serialization/Chapter09.html Type and Colour (a chapter from Building Accessible Websites, by Joe Clark)]
* [http://juicystudio.com/article/highlighting-links.php Juicy Studio: Highlighting Links]
* [http://www.maxdesign.com.au/presentation/external/ Max Design—Simple, accessible external links]
* [http://www.paciellogroup.com/resources/contrast-analyser.html Resource Center—Contrast Analyser 2.0 (Paciello Group)]
* [http://alistapart.com/articles/sprites A List Apart: CSS Sprites: Image Slicing’s Kiss of Death]

Note: This material was originally published as part of the Opera Web Standards Curriculum, available as [http://dev.opera.com/articles/view/32-styling-lists-and-links/ 32: Styling lists and links], written by [http://www.w3.org/wiki/User:Bbuchana Ben Buchanan]. Like the original, it is published under the [http://creativecommons.org/licenses/by-nc-sa/2.5/ Creative Commons Attribution, Non Commercial - Share Alike 2.5] license.

[[Category:Tutorials]]
[[Category:WSC]]