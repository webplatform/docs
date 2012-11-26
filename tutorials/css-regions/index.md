{{Page_Title|Using CSS Regions to flow content through a layout}}
{{Flags}}
{{Byline}}
{{Summary_Section|Enabling complex threaded layouts}}
{{Tutorial
|Content=The CSS Regions feature provides a way to implement complex magazine-style designs in which content flows through freely positioned layout elements. It offers you a way to dynamically flow content from one layout element to another, but does not specify how those elements are positioned. For that, use whatever CSS technique is most appropriate: floats, flexible boxes, grid layout, or absolute positioning. The following guide shows you how to flow text, but does not discuss these various layout techniques.



==Named flows==

To flow text through a document, you need a content element, a series of layout elements, and a pair of CSS properties to flow one into the other:

 article {
     flow-into: main;
 }
 div.region {
     flow-from: main;
 }

The [[css/properties/flow-into|'''flow-into''']] and [[css/properties/flow-from|'''flow-from''']] properties must both specify the same ''named flow'' for the feature to work. Once that is in place, elements assigned with [[css/properties/flow-from|'''flow-from''']] behave as ''regions'' that flow content. The series of regions through which content flows is called the ''region chain'':

[[File:region_basic.png|500px]]

Without the [[css/properties/flow-from|'''flow-from''']] property, these layout elements may contain their own independently placed content, in this case placeholder text indicating how content is supposed to be arranged:

[[File:region_layout.png|400px]]



==How flows work==

Flowing content into regions encourages you to keep ''semantic'' content element separate from the ''presentational'' elements in which they appear. Even without a corresponding region chain in which to flow, applying [[css/properties/flow-into|'''flow-into''']] makes the content element disappear from view, just as if you had assigned [[css/properties/display|'''display:none''']]. It reappears only when a corresponding [[css/properties/flow-from|'''flow-from''']] is applied to presentational elements.

While defining regions dramatically changes how content appears in the document, it's implemented entirely as CSS, and does not affect the underlying content of DOM elements. With the CSS shown above, the following displays the article's ''foo'' content within the '''div''' element, but its [[dom/properties/innerdom/innerHTML|'''innerHTML''']] is still ''bar'':

 &lt;article>foo&lt;/article>
 &lt;div class="region">bar&lt;/div>

Regions may be positioned arbitrarily around the screen, but content flows through regions strictly according to the order in which they appear in the document. Regions can be scattered across the document and interrupted by other flows' regions or non-region elements, but the only way to modify their flow order is to rearrange them in the DOM tree.

You may also specify more than one source of content, and again their order within the document determines the order in which they are presented. The example below flows ''foo'', ''bar'', and ''baz'' into the same chain of regions. Rearranging the ''article'' nodes within the document shuffles their order within output regions:

 &lt;article>foo&lt;/article>
 &lt;article>bar&lt;/article>
 &lt;article>baz&lt;/article>
 &lt;div class="region">&lt;/div>



==Controlling region breaks==

With content flowing through complex layouts, web developers need to confront design problems traditionally reserved for desktop publishing applications. While most of an article's text can be allowed to flow from one region to another, some elements such as headings should not be allowed to ''break'' so freely:

[[File:region_badbreak.png]]

Use the [[css/properties/break-before|'''break-before''']], [[css/properties/break-after|'''break-after''']], and [[css/properties/break-inside|'''break-inside''']] properties to control how content is placed relative to region breaks. This CSS forces headings into a new region:

 h1, h2, h3 {
     break-before: always;
 }

[[File:region_goodbreak.png]]

In many cases, that approach may result in too much white space within the previous region.  This alternative approach makes sure not only that headings appear unbroken within the same region, but that they don't appear isolated at the bottom of a region:

 h1, h2, h3 {
     break-after: avoid;
     break-inside: avoid;
 }

Check your target browsers' support for CSS3's [[css/properties/widows|'''widows''']] and [[css/properties/orphans|'''orphans''']] properties. They offer finer control over how many ''lines'' of text are allowed to break into another region.



==Diverting content from a flow==

The various ''break'' properties shown above don't address a common layout problem. Sometimes content needs to be diverted from a flow and moved somewhere else so that other content can flow in to take its place. In this example, '''aside''' tags represent ''pull-quote'' content to be diverted from the main flow:

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

To address this problem, note there can be more than one named flow in a document, and thus more than one series of regions. Defining a separate flow for the nested '''aside''' content removes it from the parent '''article''' content and allows for it to be placed independently. CSS and HTML such as the following...

 &lt;style>
   article         { flow-into: main;      }
   div.region      { flow-from: main;      }
   article > aside { flow-into: pullquote; }
   div.pull        { flow-from: pullquote; }
 &lt;/style>
 
 &lt;section class="page">
   &lt;div class="region"  id="title">       &lt;/div>
   &lt;div class="region"  id="intro">       &lt;/div>
   &lt;div class="region"  id="col1">        &lt;/div>
   &lt;div class="region"  id="col2_top">    &lt;/div>
   &lt;div class="pull"    id="pullquote">   &lt;/div>
   &lt;div class="region"  id="col2_bottom"> &lt;/div>
 &lt;/section>

...can produce a more fluid layout:

[[File:region_pull.png|500px]]

Note that in this example, the parent '''article''' element is assigned to the ''main'' flow, while its child '''aside''' elements are assigned to a different flow named ''pull''. You can use this same technique to assign descendant elements to the ''same'' flow.  In this example, endnotes are removed from wherever they happen to appear within the main flow of content, and are then listed at the end of the content:

 &lt;style>
   article, aside.endnote { flow-into: main }
 &lt;/style>
 
 &lt;article>
   ...
   &lt;aside class="endnote">...&lt;/aside>
   ...
   &lt;aside class="endnote">...&lt;/aside>
   ...
   &lt;h2>Endnotes&lt;/h2>
 &lt;/article>
 &lt;!-- endnotes appear here -->

However, descendant elements that are defined as the default '''flow-into:none''' cannot be prevented from flowing along with the ancestor.



==Styling region fragments==

Portions of content that break across regions are referred to as ''fragments''. Using the [[css/atrules/@region|'''@region''']] rule, fragments of content that flow into specified regions can receive custom CSS styles.

In this example, the portion of paragraph text that flows into the ''intro'' region has its text color inverted:

 @region #intro {
     p {
         color          : #fff;
     }
 }

[[Image:region_rule.png]]

To achieve the combined effect shown above, the region itself can specify its own styles. This CSS applies a different design to the ''intro'' element regardless of whether its [[css/properties/flow-from|'''flow-from''']] specifies that it behaves as a region:

 #intro {
     background-color   : #777;
 }

Not all CSS properties can be manipulated in content that flows within a region.  See [[css/atrules/@region|'''@region''']] for more information.



==Trimming overset content==

When flowing content through a layout, there may not be enough space available in the region chain to display all of it. In that case, the flow is in an ''overset'' state. By default, the last available region in the chain displays overset content according to its [[css/properties/overflow|'''overflow''']] setting. Still, even '''overflow:hidden''' leads to unfortunate visual artifacts along the bottom edge:

[[Image:region_overset_bad.png]]

The [[css/properties/region-fragment|'''region-fragment''']] CSS property controls how content displays in this situation. Setting it to '''break''' causes the last overset region to display only the fragment of content that can fit within it, just as if subsequent content flowed into another region:

 div.region {
     region-fragment: break;
     /* overflow is irrelevant within regions when above property is specified... */
     overflow: none;      
 }

This presents a much cleaner bottom edge on the overset region, and should perhaps be applied by default to all regions:

[[Image:region_overset_good.png]]

Note: The CSS Regions feature offers [[apis/css-regions|API interfaces]] that can help detect when a flow's content exceeds available layout regions, or falls short and leaves some of them empty. See the [[apis/css-regions/NamedFlow|'''NamedFlow''']] API's [[apis/css-regions/NamedFlow/overset|'''overset''']] and [[apis/css-regions/NamedFlow/firstEmptyRegionIndex|'''firstEmptyRegionIndex''']] properties, and its [[apis/css-regions/NamedFlow/regionlayoutupdate|'''regionlayoutupdate''']] event.



==Adaptive layouts with media queries==

Media queries allow you to target different designs to browsers on differently-sized devices. Such ''responsive'' web pages should target complex CSS region-based layouts only to larger-screen tablet or desktop browser interfaces. Mobile devices should rely on a much simpler one-column layout.

In the following example, large-screen browsers pour the article's content into the section's layout elements, using all the complex layout options described above. Small-screen browsers avoid the CSS Region feature altogether, suppressing the section element that would have displayed the complex layout, and also suppressing content elements (such as the pull quote) inappropriate for the simpler layout:

 @media screen and (min-width: 480px){
 
     /* pour article into section */
     article { flow-into : main; }
     section > div:not(#pull) { flow-from : main; }
 
     /* custom flow for pull quotes */
     aside { flow-into : pull; }
     div#pull { flow-from : pull; }
 
     /* @region rules can be nested within @media rules */
     @region #intro {
         p:first-of-type { color : #fff; }
     }
 }
 
 @media screen and (max-width: 480px){
 
     /* suppress layout based on CSS Regions */
     section { display : none; }
 
     /* suppress content inappropriate for mobile */
     aside { display : none; }
 
     /* style content as single column for mobile */
     article {
         margin        : 1em 1em 10em 1em;
         padding       : 1em;
         border-radius : 1em;
         background    : #fff;
     }
     body {
         background    : #aaa;
         padding       : 0;
     }
 }

This produces an alternate mobile interface:

[[Image:region_mobile.png]]

==Where to go from here==

Once you become accustomed to using regions, you can rely on a wide variety of techniques to customize layouts for your content. However, the more you want to set up rules to automate layout from various content sources, the more you should familiarize yourself with CSS3's [[tutorials/flexbox|flexible box properties]]. Support for [[tutorials/exclusions|CSS Exclusions]] allows control over how content in some layout elements flow around others. Also familiarize yourself with the [[apis/css-regions|API interfaces]] that allow JavaScript applications to control how content flows.



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
|Internet_explorer_prefixed_supported=Yes
|Internet_explorer_prefixed_version=8
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
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=8
|Note=Supports [[css/properties/flow-into|'''flow-into''']] and [[css/properties/flow-from|'''flow-from''']] properties in Compatibility Mode 5.
}}{{Compatibility Notes Row
|Browser=Internet Explorer
|Version=10
|Note=Supports [[css/properties/flow-into|'''flow-into''']] and [[css/properties/flow-from|'''flow-from''']] properties in Compatibility Mode 9.
}}
}}
{{See_Also_Section
|Topic_clusters=Regions
|External_links=* [http://html.adobe.com/webstandards/cssregions Adobe Web Standards: CSS Regions]
* [http://www.adobe.com/devnet/html5/articles/css3-regions.html CSS3 regions: Rich page layout with HTML and CSS3]
* [http://adobe.github.com/web-platform/samples/css-regions Sample pages]
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}