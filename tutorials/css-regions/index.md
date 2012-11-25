{{Page_Title|Using CSS Regions to flow content through a layout}}
{{Flags
|High-level issues=Stub
}}
{{Byline}}
{{Summary_Section|Enabling complex threaded layouts}}
{{Tutorial
|Content=CSS Regions provides a way to implement complex magazine-style designs
in which content flows through freely positioned layout elements. The
feature offers you a way to dynamically flow content from one layout
element to another, but does not specify how those elements are
positioned. For that, use whatever CSS technique is most appropriate:
floats, flexible boxes, grid layout, or absolute positioning. The
following provides a guide for how to flow text, with no discussion of
these various layout techniques.

==Named flows==

To flow text through a document, you need a content element, a series
of layout elements, and a pair of CSS properties to flow one into the
other:

 article {
     -webkit-flow-into: main;
 }
 div.region {
     -webkit-flow-from: main;
 }

The [[css/properties/flow-into|'''flow-into''']]
[[css/properties/flow-from|'''flow-from''']] properties must both
specify the same ''named flow'' for the feature to work. Once that is
in place, elements assigned with
[[css/properties/flow-from|'''flow-from''']] behave as ''regions''.
The series of regions through which content flows is called the
''region chain'':

[[File:region_basic.png|500px]]

Note there are problems with how the content flows through the layout.
The following sections clarify how to fix them.

==Separating Content and Presentation==

Flowing content into regions encourages you to keep ''semantic''
content element separate from the ''presentational'' elements in which
they appear. Even without a corresponding region chain in which to
flow, applying [[css/properties/flow-into|'''flow-into''']] makes the
content element disappear from view, just as if you had
assigned [[css/properties/display|'''display:none''']].

Oddly, while defining regions dramatically changes how content appears
in the document, it's implemented entirely as CSS, and does not affect
the underlying content of DOM elements. With the CSS shown above, the
following displays the article's ''foo'' content within the '''div'''
element, but its [[dom/properties/innerdom/innerHTML|'''innerHTML''']]
is still ''bar'':

 &lt;article>foo&lt;/article>
 &lt;div class="region">bar&lt;/div>

Regions may be positioned arbitrarily around the screen, but content
flows through regions strictly according to the order in which they
appear in the document. Regions can be scattered across the document
and interrupted by other flows' regions or non-region elements,
but the only way to modify their flow order is to rearrange them in
the DOM tree.

==Controlling Region Breaks==

With content flowing through complex layouts, web developers need to
confront design problems traditionally reserved for desktop publishing
applications. While most of an article's text can be allowed to flow
from one region to another, some elements such as headings should not
be allowed to ''break'' so freely:

[[File:region_badbreak.png]]

Use the [[css/properties/break-before|'''break-before''']],
[[css/properties/break-after|'''break-after''']], and
[[css/properties/break-inside|'''break-inside''']] properties to
control how content is placed relative to region breaks. This CSS
forces headings into a new region:

 h1, h2, h3 {
     break-before: always;
 }

[[File:region_goodbreak.png]]

In many cases, that approach may result in too much white space within
the previous region.  This alternative approach makes sure not only
that headings appear unbroken within a single region, but that they
don't appear isolated at the bottom of a region:

 h1, h2, h3 {
     break-after: avoid;
     break-inside: avoid;
 }

Note: As CSS3's [[css/properties/widows|'''widows''']] and
[[css/properties/orphans|'''orphans''']] properties are implemented,
developers will have finer control over how many ''lines'' of text are
allowed to break into another region.

==Diverting content from a flow==

The various ''break'' properties shown above don't address a common
layout problem. Sometimes content needs to be diverted from a flow and
moved somewhere else so that other content can flow in to take its
place. In this example, '''aside''' tags represent ''pull-quote''
content to be diverted from the main flow:

 &lt;article>
   &lt;h1>Sample CSS Regions Layout&lt;/h1>
   &lt;p>Riverrun, past Eve and Adam's...&lt;/p>
   &lt;p>Sir Tristram, violer d'amores...&lt;/p>
   &lt;p>The fall... of a once wallstrait oldparr...&lt;/p>
   &lt;aside>The oaks of ald now they lie in peat...&lt;/aside>
   &lt;p>What clashes here of wills gen wonts...&lt;/p>
   &lt;h2>Bygmester Finnegan, of the Stuttering Hand...&lt;/h2>
   &lt;p>...freemen's maurer, lived in the broadest way immarginable...&lt;/p>
   &lt;p>He addle liddle phifie Annie...&lt;/p>
   ...
 &lt;/article>

To address this problem, note there can be more than one named flow in
a document, and thus more than one series of regions. Defining a
separate flow for the nested '''aside''' content removes it from the
parent '''article''' content and allows for it to be placed
independently. CSS and HTML such as the following...

 &lt;style>
   article { -webkit-flow-into: main; }
   div.region { -webkit-flow-from: main; }
   article > aside { -webkit-flow-into: pullquote; }
   div.pull { -webkit-flow-from: pullquote; }
 &lt;/style>

 &lt;section class="page">
   &lt;div class="region"  id="title">       &lt;/div>
   &lt;div class="region"  id="intro">       &lt;/div>
   &lt;div class="region"  id="col1">        &lt;/div>
   &lt;div class="region"  id="col2_top">    &lt;/div>
   &lt;div class="pull"    id="col2_top">    &lt;/div>
   &lt;div class="region"  id="col2_bottom"> &lt;/div>
 &lt;/section>

...can produce a more fluid layout:

[[File:region_pull.png|500px]]

==Styling region fragments==

Portions of content that break across regions are referred to as
''fragments''. Using the [[css/atrules/@region|'''@region''']] rule,
fragments of content that flow into specified regions can receive
custom CSS styles.

In this example, the portion of paragraph text that flows into the
''intro'' region has its text color inverted:

 @region #intro {
     p {
         color          : #fff;
     }
 }

[[Image:region_rule.png]]

To achieve the combined effect shown above, the region itself can
specify its own background color:

 #intro {
     background-color   : #777;
 }

Not all CSS properties can be manipulated in content that flows within
a region.  See [[css/atrules/@region|'''@region''']] for more
information.



==More...==

[[File:region_oversetBad.png]]

[[File:region_oversetGood.png]]
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=No
|Chrome_version=
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=20
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=No
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=Yes
|Safari_prefixed_version=534
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=No
|Android_version=
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=No
|Blackberry_version=
|Blackberry_prefixed_supported=No
|Blackberry_prefixed_version=
|Chrome_mobile_supported=No
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=No
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=No
|IE_mobile_version=
|IE_mobile_prefixed_supported=No
|IE_mobile_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Regions
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}