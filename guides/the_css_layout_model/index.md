{{Page_Title|The CSS layout model: borders, boxes, margins and padding}}
{{Flags
|High-level issues=Merge Candidate
|Editorial notes=http://docs.webplatform.org/wiki/tutorials/The_CSS_layout_model_-_boxes_borders_margins_padding
}}
{{Byline}}
{{Summary_Section|This article covers the CSS layout model in some detail, including box model, borders, margin and padding, and how they all work.}}
{{Guide
|Content=== Introduction ==
 
At first glance, the CSS layout model is a straightforward affair. Boxes, borders, and margins are fairly simple objects, and CSS syntax provides a simple way to describe their characteristics.
 
However, browser rendering engines follow a long list of rules laid down in the CSS 2.1 Recommendation, and a few of their own. For this reason, there are a lot of details that need to be understood before advanced techniques can be added to a stylist’s repertoire.
 
In this article you will be introduced to the CSS properties that manipulate the layout of HTML elements, including their borders, margins, and much more. Coverage will also include some of the rules mentioned above. Advanced column layout and grid-focused techniques will be discussed in later articles that will explore form layout, floats, clearing, and positioning in greater detail. There will be many code examples linked to throughout the article to demonstrate techniques discussed, but if you want to work through the code on your local machine, you can [http://dev.opera.com/articles/view/30-the-css-layout-model-boxes-border/article30_examples.zip download all the code examples here].

== Changing composition: CSS margins, borders, and padding ==
 
Many HTML elements, such as <code>div</code> elements and headings, are rendered by default to occupy the entire width of the browser canvas and force a terminal linebreak, so that several such elements in series would render in a top-to-bottom stack on the document canvas.
 
However, HTML elements and the browser styles usually set for them are inadequate to the full range of use cases developers are called upon to consider in their work. The way CSS and HTML work together has been tuned to “fill in the gaps” so that <code>class</code>es and <code>id</code>s can add semantic meaning to markup while style sheet rules can precisely change the layout and presentation of content—perhaps even by canceling out large parts of the browser default styles altogether.
 
Careful control of whitespace is among a designer’s most important tools — and in the opinion of this author, the single most important. However, the degree of control over whitespace that brings high production values to a site design is absent from default browser stylesheets, which means that stylists typically make frequent use of the margin, border, padding, and other CSS layout properties explained in this article.
 
Margins, borders, and padding are arranged as shown in Figure 1.

[[Image:layout_fig1.png|how css layout works with margin outside the box and padding inside the box]]
 
Figure 1: An explicit illustration of the various parts of an element box, labelled with associated CSS properties.
 
=== Putting whitespace around an object: the margin-top, margin-right, margin-bottom, margin-left, and margin properties ===
 
Margins can be specified singly, or in a shorthand rule. Furthermore, the shorthand rule still allows control of individual borders around an object. Valid values are usually specified in <code>px</code> or <code>em</code> units (pixels or ems). On print-specific stylesheets <code>in</code>, <code>cm</code>, or <code>pt</code> units might be used instead (inches, centimeters or points).
 
In all cases <code>%</code> (percentage) is a valid value, but needs to be used with care; such values are calculated as a proportion of the parent element’s width, and careless provision of values might have unintended consequences. This challenge is explained in more detail during the discussion of the CSS box model below.
 
All inline elements except images lack margins, and will not take margin values. For a list of these elements, consult Table 2 below.
 
==== auto margins ====
 
Depending upon the circumstances, provision of an <code>auto</code> value instructs the browser to render a margin according to the value provided in its own stylesheet. However, when such a margin is applied to an element with a meaningful width, an <code>auto</code> margin instead causes all of the available space to be rendered as whitespace.
 
Given the following rule:
 
<syntaxhighlight lang="css">
  .narrowWaisted {
    width: 16.667em;
    margin: 1em auto 1em auto;
  }
</syntaxhighlight>
 
A block element of the <code>class</code> <code>narrowWaisted</code> will center itself in the middle of the available canvas.
 
Or the right margin of an applicable element can be set to some relatively small value, while the left margin is assigned an <code>auto</code> value.
 
When that’s done, such an element will instead appear nearly flush-right.
 
==== Negative margins ====
 
All of the margin properties can be assigned ''negative'' values. When this is done, an adjacent margin can be effectively “canceled out” to any degree. Given a large enough negative margin applied to a large enough element, the affected adjacent element can even be ''overlapped''.
 
for example, consider the following simple <code>div</code> elements (taken from [http://dev.opera.com/articles/view/30-the-css-layout-model-boxes-border/negativemargins1.html example file negativemargin1.html].)
 
<syntaxhighlight lang="css">
  <div id="header">
    <h1>Lovely header</h1>
  </div>
  <div id="content"><p>Overlapping text is entirely unreadable</p></div>
</syntaxhighlight>
 
When styled with the following CSS
 
<syntaxhighlight lang="css">
  body {
    background-color:white; font-family:Geneva, Arial, Helvetica, sans-serif;
  }

  #header { 
    background-color: yellow;
  }

  h1 { 
    color:red; 
    font-size: 2em;
  }
</syntaxhighlight>
 
It creates the output shown in Figure 2:
 
[[Image:layout_fig2.jpg|Two elements with no negative margins applied]]
 
Figure 2: The two elements from our simple example. Nothing special to see here.
 
Here comes the interesting part. Now we’ll add a fairly sizeable negative margin to the top of the bottom element, using the following rule:
 
<syntaxhighlight lang="css">#content {
  margin-top:-3em;
}
</syntaxhighlight>
 
This gives us the visual effect of shifting the element up so it overlaps with the heading, as shown in Figure 3 (see the [[negativemargins2.html example file]] for a live example).
 
[[Image:layout_fig3.jpg|Two elements with negative margins applied]]
 
Figure 3: With a negative margin applied, the bottom element shifts upwards and overlaps the heading.

==== Collapsing margins ====
 
In cases where two similar and adjacent block elements share margins that are greater than zero, only the larger of the two margins will be applied. For example, take the following rule:
 
<syntaxhighlight lang="css">
p {
  margin: 1em auto 1.5em auto;
}</syntaxhighlight>
 
If a document including this style rule is rendered ''literally'', the resulting margin between two paragraphs in series wouild be <code>2.5em</code>, as the sum of the bottom margin of paragraph 1 (1.5em) and the top margin of paragraph 2 (1em). However, due to the application of collapsing margins, the margin between them is only <code>1.5em</code>.
 
Lists and headings are peculiar among block elements, so their margins will not be collapsed into the margins of the other block elements.
 
==== Demonstration 1 ====
 
In the text styling article, the typesetting of the opening section of an F. Scott Fitzgerald story was done with many of the tools made available by CSS. For the demonstration in this article, that same page is being put to use again, with some minor changes (principally, the addition of a container element around all of the copy). The text styling is unchanged, but the few layout styles applied to that demonstration have been removed.
 
For starters, margins will be added to all of the elements that will need them.

===== Links: =====
 
* [http://dev.opera.com/articles/view/30-the-css-layout-model-boxes-border/demo_rev0.html Minimally styled demonstration document]
* [http://dev.opera.com/articles/view/30-the-css-layout-model-boxes-border/layout_00.css Beginning stylesheet]
* [http://dev.opera.com/articles/view/30-the-css-layout-model-boxes-border/demo_rev1.html New margins on body, title, pullquote, document container, and paragraphs]
* [http://dev.opera.com/articles/view/30-the-css-layout-model-boxes-border/layout_01.css Demo 1 stylesheet]

===== New rules: =====
 
<syntaxhighlight lang="css">
  body { margin: 0; }
  #main { margin: 0 auto 0 auto; }
  h1 { margin: 0 0 1em 0; }
  .pullQuote { margin: auto 0 1em 1em; }
  p { margin: 0; }
  .attribution { margin: 0 0 1.5em 0; }
</syntaxhighlight>
 
=== Adding a border to an object: border properties ===
 
There ''is'' a <code>border</code> shorthand property, but it’s only useful when you want to provide a complete and consistent border around all four sides of an element. It’s also possible to set the weight (width), style, and colour of any of an element’s four possible borders by using any meaningful combination of the following properties:
 
* <code>border-width</code>
* <code>border-style</code>
* <code>border-color</code>
* <code>border-top</code>
* <code>border-top-width</code>
* <code>border-top-style</code>
* <code>border-top-color</code>
* <code>border-right</code>
* <code>border-right-width</code>
* <code>border-right-style</code>
* <code>border-right-color</code>
* <code>border-bottom</code>
* <code>border-bottom-width</code>
* <code>border-bottom-style</code>
* <code>border-bottom-color</code>
* <code>border-left</code>
* <code>border-left-width</code>
* <code>border-left-style</code>
* <code>border-left-color</code>
 
==== The border-width properties ====
 
These properties behave exactly as one would expect: they assign explicit weight to one or more borders.
 
The <code>border-width</code> shorthand property accepts values in the same notation as the <code>margin</code> shorthand property, except that percentage values are unsupported. You might well see yourself writing a rule like the following:
 
<syntaxhighlight lang="css">td {
  border-width: 1px 0 0 1px;
}</syntaxhighlight>
 
==== The border-style properties ====
 
[[Image:figure40.png|eight different values for border style in CSS]]
 
Figure 4: the eight common border styles in action.
 
The <code>border-style</code> properties commonly accept any of the following values:

  <code>dashed</code> The length of dashes, and the amount of whitespace between them, is determined by the browser. <code>dotted</code> The amount of whitespace between dots (which may take on any shape with an aspect ratio of 1) is determined by the browser. <code>double</code> The provided width will be divided into thirds and rendered in filled-negative-filled order. <code>groove</code> An <code>outset</code> will be rendered immediately inside and flush to an <code>inset</code>. <code>inset</code> The border will be shaded to make it appear as if the element to which it is applied is depressed into the canvas. <code>none</code> Equivalent to specifying a <code>-width</code> of zero. <code>outset</code> The border will be shaded to make it appear as if the element to which it is applied extrudes from the canvas. <code>ridge</code> An <code>inset</code> will be rendered immediately inside and flush to an <code>outset</code>. <code>solid</code> The border appears as an unbroken, unshaded line.  
When the <code>border-style</code> shorthand property is used, it can accept up to four values which are applied in the same fashion as <code>margin</code> shorthand values.
 
The practice of obscuring a border (rather than omitting it) is handled by the <code>-color</code> properties.
 
==== The border-color properties ====
 
Finally, it’s possible to set any color on any individual border, with either a single property such as those listed above, or the <code>border-color</code> shorthand property. Refer to the explanation of the the <code>margin</code> shorthand property for details about the results of providing fewer than four values.
 
Like <code>background-color</code>, <code>border-color</code> can take a value of <code>transparent</code>. This can be useful in dealing with edge cases that require consistent composition but not consistent use of borders.
 
==== The border shorthand property and its four cousins, in more detail ====
 
Unlike the various <code>-width</code>, <code>-style</code>, and <code>-color</code> border properties, these five properties allow you to define the three characteristics of an object’s four borders, or of any sigle border at a time. Valid <code>border</code> (etc) shorthand values contain any or all of the width, style, and color properties that apply to that border; the only limitation is that you must refer to either one side of an element at a time, or all four at once.
 
Consider the following <code>border</code> rule:
 
<syntaxhighlight lang="css">#borderShorthandExample {
  border: 2px outset rgb(160,0,0);
  padding: .857em;
  background-color: rgb(255,224,224);
}</syntaxhighlight>
 
An element to which the above rule is applied would look exactly like this paragraph.
 
When a value is omitted from a <code>border</code> shorthand rule, the rendered element will display a default result:
 
* '''Border width''' will be determined by the browser.
* '''Border style''' will be <code>solid</code>.
* '''Border color''' will be identical to the <code>color</code> applied to the element in question.
 
==== Creating rules: the rationale for five border shorthand properties… instead of one ====
 
The “rules” discussed here are lines drawn through a layout, not directives to follow. Such lines enhance contrast between an element and its neighbouring space, and in many cases they help to create the illusion of depth within a layout. This last result is exemplified by the existence of the <code>inset</code> and <code>outset</code> border styles.

While these same effects can be accomplished by putting borders around all four sides of an element, the ability to draw precisely defined lines in a layout allows its designer considerable control over details.
 
==== …And why so many properties? They’re just borders, right? ====
 
When a layout is created which demands exceptional skill from a stylist, there will be a need to account for edge cases; this was already raised in the earlier discussion of margins.
 
Because of the way in which site designs are executed, you will encounter many cases where this element or that might have similar structural properties to other elements in a document, but have different presentation requirements. In these situations it makes perfect sense to write one rule for the most common case, and additional rules for each of the edge cases. It’s for this reason that the <code>auto</code> and <code>inherit</code> values exist: to use a default style as an edge case.
 
In the case of borders, edge cases might well require the alteration of a single characteristic of a border on a single side of an element — and when one wisely follows the KISS Principle, it’s usually best to stick to changing ''only'' those details which ''need'' to be changed.
 
==== Demonstration 2 ====
  
Certain sections of the document should be given embellishment in the form of rules and borders.
 
===== Links: =====
 
* [http://dev.opera.com/articles/view/30-the-css-layout-model-boxes-border/demo_rev2.html Add a bottom rule to the title, and a border around the pullquote]
* [http://dev.opera.com/articles/view/30-the-css-layout-model-boxes-border/layout_02.css Demo 2 stylesheet]

===== New rules: =====
 
 h1 { border-bottom: 1px solid rgb(153,153,153); }
 .pullQuote { border: 1px solid rgb(153,153,153); }

=== When margins alone aren’t enough: padding properties ===
 
You will encounter elements with background colours in secondary or accent hues that require gutters between content and margins. In other situations, you’ll need to provide space between borders and the copy near them.
 
In such cases and many others, you’ll get considerable use from the <code>padding</code>, <code>padding-top</code>, <code>padding-right</code>, <code>padding-bottom</code>, and <code>padding-left</code> properties. These properties insert negative space between the margins or borders of an element and its content. See Figure 1 above for a clear illustration of the relationship between margins, borders, and padding.
 
These properties behave in exactly the same manner as margin properties, with the following exceptions:

* <code>auto</code> values are functionally useless in references to padding properties.
* Negative padding values are invalid.
* Padding is never collapsed.
* Margin values are not applied to inline elements, but padding values are.
 
==== Demonstration 3 ====
 
Gutters should be provided for the elements to which borders were previously added.
 
===== Links: =====
 
* [http://dev.opera.com/articles/view/30-the-css-layout-model-boxes-border/demo_rev3.html Insert gutters adjacent to the borders previously put on the title and pullquote]
* [http://dev.opera.com/articles/view/30-the-css-layout-model-boxes-border/layout_03.css Demo 3 stylesheet]

===== New rules: =====
 
<syntaxhighlight lang="css">body { padding: 0; }
h1 { padding: .5em 0 .5em 0; }
.pullQuote { padding: .5em; }</syntaxhighlight>

== Working with element width and height ==
 
Most elements can have their dimensions altered as a matter of course. You’ve seen this capability demonstrated earlier in this article, during the discussion of <code>auto</code> margins.
 
The CSS properties used to manipulate the dimensions of elements are <code>width</code>, <code>height</code>, <code>min-width</code>, <code>max-width</code>, <code>min-height</code>, and <code>max-height</code>. These properties can then be divorced from (or linked to) the dimensions of element contents with the <code>overflow</code> property.
 
There’s also a <code>clip</code> property which ''hides'' parts of an element ''inside'' its margins. However, it’s omitted from this article because of its narrow scope of use.
 
=== width and height basics ===
 
As a rule, <code>width</code> and <code>height</code> produce exactly the results one would expect. However, their use carries some important caveats.
 
* '''<code>width</code> and <code>height</code> cannot be applied to <code>inline</code> elements…''' There are several elements (such as <code>span</code>, <code>strong</code>, and <code>em</code>) that will ignore the application of <code>width</code> and <code>height</code> values under typical circumstances. A list of these elements can be found in the discussion of element types, later in this article.
* '''…except for images, which can be assigned <code>width</code> and <code>height</code> even though they are inline elements.''' The CSS 2.1 Recommendation refers to images as “replaced” elements, which means that the browsers should always treat them as possessing static dimensions.  For this reason, those dimensions can be arbitrarily altered.
* '''<code>width</code> and <code>height</code> are only two of the properties that can influence the functional dimensions of an element.''' As a result, it’s easy to put yourself in situations where an element is too small (usually too narrow) to hold its content as expected, leading to blowouts.  The CSS box model discussion below addresses this issue.
* '''Rendering bugs in Microsoft Internet Explorer (IE) make it necessary to specify explicit <code>width</code> or <code>height</code> property/value pairs for some elements.''' There are some peculiarities about IE’s rendering engine that can only be resolved with brute force (see the Glossary).  Most of these peculiarities are known and slated to be removed from IE 8, but until that version has replaced its predecessors within the IE install base, this issue will be an inevitable test case.  [http://www.positioniseverything.net/ PositionIsEverything.net] and the [http://css-discuss.incutio.com/ CSS-Discuss Wiki] provide ample information about this issue and techniques that work around it.
* '''Rounding algorithms will, from time to time, cause off-spec differences in layout between browsers which display content via LCD, LED, or CRT (<code>type="screen"</code>) display media.''' The <code>screen</code> media type ultimately requires all units to be coverted into pixel measurements, which may map differently from one browser to the next.

=== min-width, max-width, min-height, and max-height ===
 
From time to time you will encounter situations in which you need to constrain the size of an element — usually to ensure that a proportionally-sized column will always retain a readable width. The various <code>min-</code> and <code>max-</code> properties answer this requirement. As is the case with <code>width</code> and <code>height</code>, the results one can expect from using these properties are fairly predictable as a matter of course.
 
However, in the experience of this author, these properties have limited use (although other authors disagree). Like plain old <code>width</code> and <code>height</code>, they’re subject to rounding errors that can deliver entirely unexpected results. More importantly, they are completely unsupported in IE 6, which still holds a considerable market share as of July 2008.
 
==== Demonstration 4 ====
 
<code>auto</code> margins were placed to the left and right of the page container. Now it needs a <code>width</code> for those margin values to make any sense. Furthermore, the plan is to assign a <code>float</code> value to the pullquote, so that’ll get a width, too.
 
===== Links: =====
 
* [http://dev.opera.com/articles/view/30-the-css-layout-model-boxes-border/demo_rev4.html Change the width of the document container and the pullquote]
* [http://dev.opera.com/articles/view/30-the-css-layout-model-boxes-border/layout_04.css Demo 4 stylesheet]

===== New rules: =====
 
<syntaxhighlight lang="css">#main { width: 42em; }
.pullQuote { width: 14em; }</syntaxhighlight>
 
=== overflow: fencing in content, or setting it free ===
 
When an element’s <code>width</code> or <code>height</code> are set, it’s sometimes necessary to consider what results are desired in the event that the contents of that element take up more space than is strictly available. This is especially true on sites with both user generated content and strict layout specifications.
 
The <code>overflow</code> property and its four valid values — <code>visible</code>, <code>hidden</code>, <code>auto</code>, and <code>scroll</code> — are provided to handle such circumstances. Figure 5 illustrates the effect they have when applied to an element whose content spills out of its bounding box.
 
[[Image:figure50.png|the effects of the CSS overflow property]]

Figure 5: The effects of the CSS overflow property.
 
==== The results of the four overflow values ====
  <code>visible</code> '''(default)''' Contents beyond the available dimensions of an element are displayed ''without'' affecting the flow or margins of adjacent elements. Consequently, content of one element may appear to ''collide'' with the content of its neighbours. Techniques for avoiding this outcome and special cases caused by rendering issues in IE are discussed in later articles. <code>hidden</code> Any content which lies beyond the bounds of an element will be hidden from view. <code>auto</code> The dimensions of an element will be constrained just as when the <code>hidden</code> value is used, except that scrollbars will be created as needed to make overflowing content accessible to the visitor. <code>scroll</code> Both vertical and horizontal scrollbars will be incorporated into the element, even if they’re not needed.  

== The CSS box models: fitting everything together ==
 
Now that the fundamental layout properties have been covered, it’s time to discover how the width of an element is rendered by the browser according to its CSS properties — and how to keep elements from blowing out your layouts. Some results will make perfect sense, while others will seem horribly counter-intuitive. To complicate matters, there are actually two layout algorithms to consider: the model specified by the World Wide Web Consortium (W3C) in the CSS 2.1 Recommendation, and the one used in older versions of IE.
 
=== Choosing the right units for your layout ===
 
As in the case of text, elements can be sized with either proportional units such as <code>%</code> or <code>em</code>, or static units like <code>px</code>. Something else to consider is that the browser canvas is always sized at a static value that cannot be assumed without using client-side script code to either retrieve that size, or resize the window — techniques which are ill-suited to the demands of accessibility, usability, and media portability.
 
==== The principal rule of sizing elements: mix proportional and static units with care, or not at all ====
 
The default value for both <code>width</code> and <code>height</code> is <code>auto</code>, which in Standard English is a directive to “use the available space.” The result for block elements is that their computed <code>width</code> occupies ''all'' of that space. With respect to <code>height</code>, elements expand to enclose their content by default.
 
If you change <code>width</code> and <code>height</code> values, you must then be careful to ensure that the contents of an element will fit (with their margins, borders, and padding) into the width you’ve specified. The easiest way to do this by engaging in the following process:
 
# Consider the largest maximum width likely to be available for your layout, given common display resolutions and/or type sizes.  As of this writing, this measurement will typically be something around 800 or 1024 pixels.  The broader the expected audience of your site, the more likely it is that the smaller of these values should be chosen.
# Create a container element for your entire document that is set to an expected width less than the width worked out in step #1.
# Use the same unit type when setting layout properties for the elements within the container element created in step #2.
 
==== Choosing the right unit type for layout: advantages and disadvantages ====
                          
{{{!}} border="1"
{{!}}-
!Unit
!Advantages
!Disadvantages
{{!}}-
!em
{{!}}
* Best suited to creating highly precise layout grids in two dimensions
* When used in relation to document containers, makes possible layouts that expand or contract according to the size of body copy
* The computed dimensions of elements become easily predictable
{{!}}
* Fractional units might expand or contract with slight differences between browsers
* To achieve the best results, all <code>font-size</code> and <code>line-height</code> values in the document should be set to explicit and predictable values
{{!}}-
!percentage
{{!}}
* Best suited to ''completely'' flexible layouts
* Easiest for creating things like equal columns
{{!}}
* Blowout avoidance might require extra container elements
* Might result in unacceptably wide or narrow elements
* Results are highly dependent on context (see discussion of the box models below)
{{!}}-
!px
{{!}}
* Offers the greatest amount of control over layout
* Eliminates most cross-browser variation in layout
{{!}}
* Most ill-suited to accessibility and cross-media support requirements
* Most susceptible to blowouts
{{!}}} 

Table 1: Advantages and disadvantages of the percentage, em, and pixel units in specifying layout properties.
 
=== The box model components ===
 
The box model is really just a series of directives that define how the various layout specifications of an element interact with one another. The components covered by the box model are:
 
# document canvas
# margins
# borders
# padding
# element widths and heights
# child element properties
 
The last of these items in turn includes the other five. However, for simplicity’s sake this section will focus on simple parent-child element relationships, and reserve discussion of multi-level box model interactions for later articles that will delve into the finer points of page layout.
 
=== The W3C box model: everything is additive ===
 
The basic rule is that the computed width or height of an element is equal to:
 
<code>margin + border + padding + (width{{!}}height)</code>
 
In many cases the <code>width</code> and/or <code>height</code> will be set to its default value of <code>auto</code>, meaning that the canvas area put aside for content is equal to:
 
<code>available_canvas − margin − padding − border</code>
 
In such an equation, <code>available_canvas</code> is itself a discrete (if often auto-computed) value, less the amount of margins, borders and padding. This number is most important for the ''width'' of elements, because width calculation errors on the part of a designer will have the undesirable result of causing a horizontal scrollbar to appear in the browser window. Additionally, browsers always place elements at the left margin of the browser canvas that would otherwise overflow beyond the right margin of the browser window, unless instructed to do otherwise.
 
Consider the following style sheet rule:
 
<syntaxhighlight lang="css">#myLayoutColumn {
  width: 50em;
  margin: 1.5em auto 1.5em auto;
  border: .1em;
  padding: .9em;
}
</syntaxhighlight>
 
As discussed during the explanation of margin properties above, one can expect <code>#myLayoutColumn</code> to center itself within its container element, whether that container is <code>body</code>, or something created by the production team.
 
Furthermore, if the activation of “strict mode” (through the use of an appropriate <code>!DOCTYPE</code> declaration) causes the W3C box model to be used, one can also expect the computed ''non-marginal'' width to be:
 
<code>.1em + .9em + 50em + .9em + .1em = 52em</code>
 
In <code>screen</code> media the browser will then take this value, round all of the values separately to the nearest pixel, and render the result accordingly.
 
==== Proportional margins and padding in the W3C box model ====
 
When the W3C box model is in use, proportional margins and padding are computed relative to the computed <code>width</code> of the ''containing'' element. To give one example, if you specify <code>margin: 20%</code> for an element that’s contained within an element that is 800 pixels wide, the margin rendered around the first element will be 160 pixels on all sides (as 20% of 800 is 160).
 
If that same element is assigned <code>padding: 5%</code>, its computed content width will be 400 pixels:
 
<pre>20% + 5% + 5% + 20% = ''50%'' ''0.50'' × 800 = ''400''
800 − ''400'' = ''400''</pre>
 
== Working with document flow ==
 
Upcoming tutorials discuss the creation of multi-column layouts, so there are three CSS properties left to introduce in this article: <code>display</code>, <code>float</code>, and <code>clear</code>.
 
=== Element types and the display property ===
 
With the exception of <code>html</code>, <code>body</code>, and <code>table</code> parts, each element in the HTML 4.01 Recommendation that relates to primary content has an associated type of inline or block. Each type determines default layout behaviour in different ways:

==== Inline ====  

* Text and images that immediately follow and/or precede inline elements are rendered on a common baseline with the content of the inline element, unless they're so long that they would otherwise overlap the edge of the containing element, in which case the inline content will wrap onto a new baseline underneath the first one.
* Lines of text within inline elements are laid out with soft linebreaks as needed (or allowed), except where this behaviour is modified by use of the <code>white-space</code> property.
* <code>margin</code>, <code>width</code>, <code>height</code>, and <code>float</code> properties in style sheet rules applicable to these elements (except <code>img</code> and <code>object</code>) are ignored.
* Inline elements can only contain text or other inline elements.

==== Block ====  

* These elements are rendered as discrete blocks within their containers.
* Unless assigned a <code>float</code> value of <code>left</code> or <code>right</code>, will always be rendered with preceding and following linebreaks.
* Linebreaks between nested block elements that don’t have any content between them will typically be collapsed.
* block elements with a width of <code>auto</code> (the default) will always expand to fill the entire width available to them.
   
The <code>display</code> property has three commonly used values — <code>block</code>, <code>inline</code>, and <code>none</code> — of which two refer to the corresponding element types. The effect of changing an element’s <code>display</code> value is to cause an inline element to behave like a block element, to make a block element behave like an inline one, or to alter the rendering of the document as if the element (and all of its contents) did not exist at all.
 
As a matter of course, it’s vital to know which elements correspond to which types by default, relationships laid out briefly in Table 2:
                                                                                                                                                
{{{!}} border="1"
{{!}}-
!Element
!Type
!Subtype
!Notes
{{!}}-
!<code>a</code>
{{!}}inline
{{!}}special
{{!}} 
{{!}}-
!<code>abbr</code>
{{!}}inline
{{!}}phrase
{{!}} 
{{!}}-
!<code>acronym</code>
{{!}}inline
{{!}}phrase
{{!}} 
{{!}}-
!<code>address</code>
{{!}}block
{{!}} 
{{!}}Behaves similarly to <code>p</code> in common practice
{{!}}-
!<code>blockquote</code>
{{!}}block
{{!}} 
{{!}}Must contain at least one block element when the declared <code>!DOCTYPE</code> is <code>Strict</code>
{{!}}-
!<code>body</code>
{{!}} 
{{!}} 
{{!}}Encloses the entire document canvas; commonly takes on a margin (in IE, Firefox, and Safari) or padding (in Opera) of <code>10px</code> in <code>screen</code> media
{{!}}-
!<code>cite</code>
{{!}}inline
{{!}}phrase
{{!}} 
{{!}}-
!<code>div</code>
{{!}}block
{{!}} 
{{!}} 
{{!}}-
!<code>em</code>
{{!}}inline
{{!}}phrase
{{!}} 
{{!}}-
!<code>fieldset</code>
{{!}}block
{{!}} 
{{!}}Commonly rendered by default with <code>border: 1px black;</code>
{{!}}-
!<code>form</code>
{{!}}block
{{!}} 
{{!}} 
{{!}}-
!<code>h1 … h6</code>
{{!}}block
{{!}}heading
{{!}} 
{{!}}-
!<code>input</code>
{{!}}inline
{{!}}formctrl
{{!}} 
{{!}}-
!<code>img</code>
{{!}}inline
{{!}}special
{{!}} 
{{!}}-
!<code>label</code>
{{!}}inline
{{!}}formctrl
{{!}} 
{{!}}-
!<code>li</code>
{{!}}block
{{!}} 
{{!}}Element type not specified in Document Type Definition, but this element may contain either block or inline elements; the complete CSS 2.1 Recommendation sets aside a <code>display</code> value for list items
{{!}}-
!<code>ol</code>
{{!}}block
{{!}}list
{{!}} 
{{!}}-
!<code>p</code>
{{!}}block
{{!}} 
{{!}}May only contain inline elements; commonly rendered with top and bottom margins
{{!}}-
!<code>span</code>
{{!}}inline
{{!}}special
{{!}} 
{{!}}-
!<code>strong</code>
{{!}}inline
{{!}}phrase
{{!}} 
{{!}}-
!<code>table</code>
{{!}}block
{{!}} 
{{!}} 
{{!}}-
!<code>ul</code>
{{!}}block
{{!}}list
{{!}} 
{{!}}} 

Table 2: Frequently used HTML elements and their types. Only margins between two adjacent block elements of the same subtype will collapse.

==== Demonstration 5 ====
 
How about removing the “Prologue” annotation from the title, just for demonstration’s sake?
 
===== Links: =====
 
* [http://dev.opera.com/articles/view/30-the-css-layout-model-boxes-border/demo_rev5.html Remove the extraneous bit from the title]
* [http://dev.opera.com/articles/view/30-the-css-layout-model-boxes-border/layout_05.css Demo 5 stylesheet]

===== New rules: =====
 
<syntaxhighlight lang="css">.sectionNote { display: none; }</syntaxhighlight>
 
=== Causing elements to flow around others: the float property ===

[[Image:box_baco.jpg|a cat with bacon taped to his back]] 

A photo is positioned to the left of this paragraph. Practically all of you will see that the following copy flows naturally ''around'' it, though some might need first to cease wondering why a well-known science fiction novelist would tape bacon to his cat—even if he was having a slow day. HTML attributes can be used to specify the layout behaviour you see, but in this instance the results were accomplished with CSS.
 
As one can imagine, the property/value pair that works this magic is <code>float: left;</code>. The finer points of working with floats will be addressed in later articles, but it’s necessary to touch on the basics here. <code>float: right</code> is also a perfectly serviceable property/value pair, and for those occasions when you need to contradict a <code>class</code> assignment that invokes <code>float</code>, you can specify <code>float: none</code>.
 
The <code>float</code> property ''does'' come with a few use instructions:
 
* A <code>float</code> value will only matter if it’s applied to a block element with an explicit <code>width</code>.
* <code>float</code>, <code>clear</code>, and <code>margin</code> properties all appear ''together'' in style sheet rules meant to create columns within a layout.
* Causing a floated element to stretch to the bottom of its container is a tricky matter, but not impossible. The common way to do this is referred to as [http://www.alistapart.com/articles/fauxcolumns/ faux-columns].
 
==== Demonstration 6 ====
 
Placement of a <code>float</code> value on the pullquote has been talked about, so now it gets done and the results can be seen. While we're at it, let's add some background colour to help distinguish it from the main content.
 
===== Links: =====
 
* [http://dev.opera.com/articles/view/30-the-css-layout-model-boxes-border/demo_rev6.html Float the pullquote over at the right margin]
* [http://dev.opera.com/articles/view/30-the-css-layout-model-boxes-border/layout_06.css Demo 6 stylesheet]

===== New rules: =====
 
<syntaxhighlight lang="css">.pullQuote { float: right;
background-color: rgb(204,204,204); }
</syntaxhighlight>
 
=== Forcing elements below their floated predecessors: the clear property ===
 
Like the <code>float</code> property, the <code>clear</code> property can be assigned one of the <code>left</code>, <code>right</code>, or <code>none</code> values. The <code>both</code> value is also supported.
 
While the <code>float</code> property directs how the content of subsequent elements should flow around it, the <code>clear</code> property directs how an element should flow around all of its neighbours—in many practical cases, not at all.
 
Figure 6 illustrates the behaviour of <code>clear: left;</code> in a layout where two initial consecutive elements have been assigned identical <code>height</code> values, and <code>float</code> values of <code>left</code> and <code>right</code>:
 
[[Image:figure60.png|clear left allows the bottom box to clear both columns as they are the same height]]
 
Figure 6: <code>clear:left </code> allows the bottom box to clear both columns, as they are the same height.

In the preceding demonstration, the ''default'' flow of <code>#cLeftWidget</code> would place it just below the Latin text — that is, ''between'' <code>#fLeftWidget</code> and <code>#fRightWidget</code>.
 
Consider what happens when the first of the same collection of elements is made shorter than its flush-right sibling, as seen in Figure 7.
 
[[Image:figure70.png|When the right column is longer than the left column clear left will not clear both columns and so clear both must be used instead]]
 
Figure 7: When the right column is longer than the left column, <code>clear:left </code> will not clear both columns and so <code>clear:both </code> must be used instead
 
In the first example, the <code>clear</code> value of the trailing element is set to <code>left</code> in order to make a point: because both of the <code>float</code>ed elements are the same height, the <code>clear</code>ed element will be pushed below both. However, the second example proves that in order to achieve the same result with <code>float</code>ed elements of differing heights, <code>clear: both;</code> must be used.
 
This discussion of the <code>clear</code> property is intended as a simple introduction to its effects, while later articles discuss the finer points of technique associated with its use.
 
== Summary ==
 
Between differences in rendering engines, the need to cover a wide swathe of traditionally defined ground, and the inability to predict the certain dimensions of a browser window, the layout of Web documents is fraught with hassles and caveats. However, the common level of CSS support has advanced to the point where Web documents are not hard to get to give decent results across browsers.
|height)</code>
 
In many cases the <code>width</code> and/or <code>height</code> will be set to its default value of <code>auto</code>, meaning that the canvas area put aside for content is equal to:
 
<code>available_canvas − margin − padding − border</code>
 
In such an equation, <code>available_canvas</code> is itself a discrete (if often auto-computed) value, less the amount of margins, borders and padding_ This number is most important for the ''width'' of elements, because width calculation errors on the part of a designer will have the undesirable result of causing a horizontal scrollbar to appear in the browser window_ Additionally, browsers always place elements at the left margin of the browser canvas that would otherwise overflow beyond the right margin of the browser window, unless instructed to do otherwise_
 
Consider the following style sheet rule:
 
<pre>#myLayoutColumn {
  width: 50em;
  margin: 1_5em auto 1_5em auto;
  border: _1em;
  padding: _9em;
}</pre>
 
As discussed during the explanation of margin properties above, one can expect <code>#myLayoutColumn</code> to center itself within its container element, whether that container is <code>body</code>, or something created by the production team_
 
Furthermore, if the activation of “strict mode” (through the use of an appropriate <code>!DOCTYPE</code> declaration) causes the W3C box model to be used, one can also expect the computed ''non-marginal'' width to be:
 
<code>_1em + _9em + 50em + _9em + _1em=52em</code>
 
In <code>screen</code> media the browser will then take this value, round all of the values separately to the nearest pixel, and render the result accordingly.
 
==== Proportional margins and padding in the W3C box model ====
 
When the W3C box model is in use, proportional margins and padding are computed relative to the computed <code>width</code> of the ''containing'' element. To give one example, if you specify <code>margin: 20%</code> for an element that’s contained within an element that is 800 pixels wide, the margin rendered around the first element will be 160 pixels on all sides (as 20% of 800 is 160).
 
If that same element is assigned <code>padding: 5%</code>, its computed content width will be 400 pixels:
 
<pre>20% + 5% + 5% + 20% = ''50%'' ''0.50'' × 800 = ''400''
800 − ''400'' = ''400''</pre>
 
== Working with document flow ==
 
Upcoming tutorials discuss the creation of multi-column layouts, so there are three CSS properties left to introduce in this article: <code>display</code>, <code>float</code>, and <code>clear</code>.
 
=== Element types and the display property ===
 
With the exception of <code>html</code>, <code>body</code>, and <code>table</code> parts, each element in the HTML 4.01 Recommendation that relates to primary content has an associated type of inline or block. Each type determines default layout behaviour in different ways:

==== Inline ====  

* Text and images that immediately follow and/or precede inline elements are rendered on a common baseline with the content of the inline element, unless they're so long that they would otherwise overlap the edge of the containing element, in which case the inline content will wrap onto a new baseline underneath the first one.
* Lines of text within inline elements are laid out with soft linebreaks as needed (or allowed), except where this behaviour is modified by use of the <code>white-space</code> property.
* <code>margin</code>, <code>width</code>, <code>height</code>, and <code>float</code> properties in style sheet rules applicable to these elements (except <code>img</code> and <code>object</code>) are ignored.
* Inline elements can only contain text or other inline elements.

==== Block ====  

* These elements are rendered as discrete blocks within their containers.
* Unless assigned a <code>float</code> value of <code>left</code> or <code>right</code>, will always be rendered with preceding and following linebreaks.
* Linebreaks between nested block elements that don’t have any content between them will typically be collapsed.
* block elements with a width of <code>auto</code> (the default) will always expand to fill the entire width available to them.
   
The <code>display</code> property has three commonly used values — <code>block</code>, <code>inline</code>, and <code>none</code> — of which two refer to the corresponding element types. The effect of changing an element’s <code>display</code> value is to cause an inline element to behave like a block element, to make a block element behave like an inline one, or to alter the rendering of the document as if the element (and all of its contents) did not exist at all.
 
As a matter of course, it’s vital to know which elements correspond to which types by default, relationships laid out briefly in Table 2:
                                                                                                                                                
{{{!}} border="1"
{{!}}-
!Element
!Type
!Subtype
!Notes
{{!}}-
!<code>a</code>
{{!}}inline
{{!}}special
{{!}} 
{{!}}-
!<code>abbr</code>
{{!}}inline
{{!}}phrase
{{!}} 
{{!}}-
!<code>acronym</code>
{{!}}inline
{{!}}phrase
{{!}} 
{{!}}-
!<code>address</code>
{{!}}block
{{!}} 
{{!}}Behaves similarly to <code>p</code> in common practice
{{!}}-
!<code>blockquote</code>
{{!}}block
{{!}} 
{{!}}Must contain at least one block element when the declared <code>!DOCTYPE</code> is <code>Strict</code>
{{!}}-
!<code>body</code>
{{!}} 
{{!}} 
{{!}}Encloses the entire document canvas; commonly takes on a margin (in IE, Firefox, and Safari) or padding (in Opera) of <code>10px</code> in <code>screen</code> media
{{!}}-
!<code>cite</code>
{{!}}inline
{{!}}phrase
{{!}} 
{{!}}-
!<code>div</code>
{{!}}block
{{!}} 
{{!}} 
{{!}}-
!<code>em</code>
{{!}}inline
{{!}}phrase
{{!}} 
{{!}}-
!<code>fieldset</code>
{{!}}block
{{!}} 
{{!}}Commonly rendered by default with <code>border: 1px black;</code>
{{!}}-
!<code>form</code>
{{!}}block
{{!}} 
{{!}} 
{{!}}-
!<code>h1 … h6</code>
{{!}}block
{{!}}heading
{{!}} 
{{!}}-
!<code>input</code>
{{!}}inline
{{!}}formctrl
{{!}} 
{{!}}-
!<code>img</code>
{{!}}inline
{{!}}special
{{!}} 
{{!}}-
!<code>label</code>
{{!}}inline
{{!}}formctrl
{{!}} 
{{!}}-
!<code>li</code>
{{!}}block
{{!}} 
{{!}}Element type not specified in Document Type Definition, but this element may contain either block or inline elements; the complete CSS 2.1 Recommendation sets aside a <code>display</code> value for list items
{{!}}-
!<code>ol</code>
{{!}}block
{{!}}list
{{!}} 
{{!}}-
!<code>p</code>
{{!}}block
{{!}} 
{{!}}May only contain inline elements; commonly rendered with top and bottom margins
{{!}}-
!<code>span</code>
{{!}}inline
{{!}}special
{{!}} 
{{!}}-
!<code>strong</code>
{{!}}inline
{{!}}phrase
{{!}} 
{{!}}-
!<code>table</code>
|block
{{!}} 
{{!}} 
{{!}}-
!<code>ul</code>
{{!}}block
{{!}}list
{{!}} 
{{!}}} 

Table 2: Frequently used HTML elements and their types. Only margins between two adjacent block elements of the same subtype will collapse.

==== Demonstration 5 ====
 
How about removing the “Prologue” annotation from the title, just for demonstration’s sake?
 
===== Links: =====
 
* [http://dev.opera.com/articles/view/30-the-css-layout-model-boxes-border/demo_rev5.html Remove the extraneous bit from the title]
* [http://dev.opera.com/articles/view/30-the-css-layout-model-boxes-border/layout_05.css Demo 5 stylesheet]

===== New rules: =====
 
<pre>.sectionNote { display: none; }
</pre>
 
=== Causing elements to flow around others: the float property ===

[[Image:box_baco.jpg|a cat with bacon taped to his back]] 

A photo is positioned to the left of this paragraph. Practically all of you will see that the following copy flows naturally ''around'' it, though some might need first to cease wondering why a well-known science fiction novelist would tape bacon to his cat—even if he was having a slow day. HTML attributes can be used to specify the layout behaviour you see, but in this instance the results were accomplished with CSS.
 
As one can imagine, the property/value pair that works this magic is <code>float: left;</code>. The finer points of working with floats will be addressed in later articles, but it’s necessary to touch on the basics here. <code>float: right</code> is also a perfectly serviceable property/value pair, and for those occasions when you need to contradict a <code>class</code> assignment that invokes <code>float</code>, you can specify <code>float: none</code>.
 
The <code>float</code> property ''does'' come with a few use instructions:
 
* A <code>float</code> value will only matter if it’s applied to a block element with an explicit <code>width</code>.
* <code>float</code>, <code>clear</code>, and <code>margin</code> properties all appear ''together'' in style sheet rules meant to create columns within a layout.
* Causing a floated element to stretch to the bottom of its container is a tricky matter, but not impossible. The common way to do this is referred to as [[faux-columns]].
 
==== Demonstration 6 ====
 
Placement of a <code>float</code> value on the pullquote has been talked about, so now it gets done and the results can be seen. While we're at it, let's add some background colour to help distinguish it from the main content.
 
===== Links: =====
 
* [http://dev.opera.com/articles/view/30-the-css-layout-model-boxes-border/demo_rev6.html Float the pullquote over at the right margin]
* [http://dev.opera.com/articles/view/30-the-css-layout-model-boxes-border/layout_06.css Demo 6 stylesheet]

===== New rules: =====
 
<pre>.pullQuote { float: right;
background-color: rgb(204,204,204); }
</pre>
 
=== Forcing elements below their floated predecessors: the clear property ===
 
Like the <code>float</code> property, the <code>clear</code> property can be assigned one of the <code>left</code>, <code>right</code>, or <code>none</code> values. The <code>both</code> value is also supported.
 
While the <code>float</code> property directs how the content of subsequent elements should flow around it, the <code>clear</code> property directs how an element should flow around all of its neighbours—in many practical cases, not at all.
 
Figure 6 illustrates the behaviour of <code>clear: left;</code> in a layout where two initial consecutive elements have been assigned identical <code>height</code> values, and <code>float</code> values of <code>left</code> and <code>right</code>:
 
[[Image:figure60.png|clear left allows the bottom box to clear both columns as they are the same height]]
 
Figure 6: <code>clear:left </code> allows the bottom box to clear both columns, as they are the same height.

In the preceding demonstration, the ''default'' flow of <code>#cLeftWidget</code> would place it just below the Latin text — that is, ''between'' <code>#fLeftWidget</code> and <code>#fRightWidget</code>.
 
Consider what happens when the first of the same collection of elements is made shorter than its flush-right sibling, as seen in Figure 7.
 
[[Image:figure70.png|When the right column is longer than the left column clear left will not clear both columns and so clear both must be used instead]]
 
Figure 7: When the right column is longer than the left column, <code>clear:left </code> will not clear both columns and so <code>clear:both </code> must be used instead
 
In the first example, the <code>clear</code> value of the trailing element is set to <code>left</code> in order to make a point: because both of the <code>float</code>ed elements are the same height, the <code>clear</code>ed element will be pushed below both. However, the second example proves that in order to achieve the same result with <code>float</code>ed elements of differing heights, <code>clear: both;</code> must be used.
 
This discussion of the <code>clear</code> property is intended as a simple introduction to its effects, while later articles discuss the finer points of technique associated with its use.
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|External_links=* Bergevin, Holly, and Gallant, John. 2006. [http://positioniseverything.net/explorer.html Explorer exposed]. Position Is Everything. (accessed 1 July 2008).
* Bos, Bert, ''et al.'' 2007. [http://www.w3.org/TR/2007/CR-CSS21-20070719 Cascading style sheets level 2 revision 1 (CSS 2.1) specification]. World Wide Web Consortium. ''etc.'' (accessed 30 June 2008).
* Raggett, Dave, ''et. al''. 1999. [http://www.w3.org/TR/1999/REC-html401-19991224 HTML 4.01 specification]. World Wide Web Consortium. ''etc.'' (accessed 30 June 2008).
* Raymond, Eric, and Steele, Guy, eds. 2003. [http://www.catb.org/jargon/html/B/brute-force.html Brute force]. The Jargon File (Version 4.4.7). (accessed 30 June 2008).
* Scalzi, John. 2006. [http://www.scalzi.com/whatever/004457.html Clearly you people thought I was kidding]. Whatever. (accessed 30 June 2008).
|Manual_sections==== Exercise questions ===
 
# Under which circumstances is it best to use the shorthand <code>margin</code> value, or a single margin property such as <code>margin-top</code>?
# When the shorthand <code>margin</code>, <code>padding</code>, and <code>border-width</code> properties are provided with all four values, in what order are those values applied to the four sides of an element?
# If you want to place a rule under the text of each heading in a document, which property would you use?
# Which <code>border-style</code> value would you use to give an element an appearance like an interface button?
# ''Yes or no:'' Will specifying a border around an element will also provide for a gutter around the content of that element, by default?
# If you create an element that isn’t as wide as its container, which property/value pair do you need to set to ensure that the element is horizontally centered within its container?
# ''Yes or no:'' If you place a container element within <code>body</code> and set its <code>width</code> to a value greater than <code>100%</code>, will the behaviour of the document canvas change?
# If an image is too large for its containing element, which property/value pair would you use to ensure that your page layout doesn’t blow out, and why?
# If you assign a <code>display</code> value of <code>block</code> to an <code>a</code> (link) element and give that element a reasonable height and width, how does the mouseover behaviour of that link change in <code>screen</code> display media?
# Under normal circumstances, a block element expands to fill the width of its container (less margins, borders, and padding). By default, does this behaviour truly change when that element is preceded by a <code>float</code>ed element — or merely ''appear'' to change?
# If you intend to apply a <code>float</code> value to an element, which other property must you also set on that element?
# If you wanted to make ''absolutely'' sure that an element would ''always'' expand to fill the width of its container, which property/value pairs would you set?
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=DevOpera
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}