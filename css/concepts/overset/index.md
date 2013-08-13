{{Page_Title|overset content}}
{{Flags
|Checked_Out=No
}}
{{API_Name}}
{{Summary_Section|Refers to a situation in which the final [[css/concepts/region|''region'']] of a [[css/concepts/region_chain|''region chain'']] is unable to fully display remaining content of a [[css/concepts/named_flow|''named flow'']].}}
{{Concept_Page
|Content=The ''CSS Regions'' feature allows content to flow dynamically through
a series of presentational block elements, known as
[[css/concepts/region|''regions'']], allowing for complex
magazine-style layouts. This [[css/concepts/region_chain|''region
chain'']] may not have enough room to accommodate all the content.  In
that case, illustrated below as ''Scenario #2'', the final region is in an
[[css/concepts/overset|''overset'']] state, as is the
[[css/concepts/named_flow|''named flow'']] that contains all the
content.

Depending on its
[[css/properties/region-fragment|'''region-fragment''']] property, the
final [[css/concepts/region|region's]] content may appear as a
[[css/concepts/fragment|''fragment'']], breaking cleanly as if there
were subsequent regions in the chain into which content could flow.
Otherwise it may simply ''overflow'' the final element: either
clipping, spilling, or scrolling past the element's dimensions as specified
by the region's [[css/properties/overflow|'''overflow''']] property.

There are two ways to programatically detect overset state:

* From the content side, if the [[css/concepts/named_flow|named flow's]] [[apis/css-regions/NamedFlow/overset|'''overset''']] property is '''true''', it means that it doesn't fully display within the [[css/concepts/region_chain|region chain]], or that it has not been placed within any [[css/concepts/region|regions]].

* On the presentation side, if the final region element's [[apis/css-regions/Region/regionOverset|'''regionOverset''']] property is '''overset''', some of its content can flow into another region if available.

For an overview of CSS Regions, see [[tutorials/css-regions|Using CSS Regions to flow content through a layout]].
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This defines a set of content and a region chain into which to present it:
|Code=<syntaxhighlight language="html">
<style>
article.content { flow-into: main;}
section.layout > div { flow-from: main; }
</style>

<!-- CONTENT -->

<article class="content">
  <p>Content #1</p>
  <p>Content #2</p>
  ...
  <p>Content #n</p>
  <p>Final Content</p>
</article>

<!-- LAYOUT -->

<section class="layout">
  <div>Region #1</div>
  <div>Region #2</div>
  <div>Region #3</div>
  <div>Region #4</div>
</section>
</syntaxhighlight>
}}{{Single Example
|Language=HTML
|Description=''Scenario #1:'' If the region provides enough area, the final content element appears within the final region. The final '''div''' element's [[apis/css-regions/Region/regionOverset|'''regionOverset''']] property returns '''fit'''. Note that this is ''not'' valid DOM structure, and simply illustrates how content [[css/concepts/fragment|''fragments'']] appear dynamically within the region chain.
|Code=<syntaxhighlight language="html">
<section class="layout">
  <div>
      	    <article class="content">
              <p>Content #1</p>
              <p>Content...
  </div>
  <div>
              ...#2</p>
  </div>
  <div>
              ...
              <p>Content #n</p>
  </div>
  <div>
              <p>Final Content</p>
      	     </article>
  </div>
</section>
</syntaxhighlight>
}}{{Single Example
|Language=HTML
|Description=''Scenario #2:'' This shows the same situation, but with not enough area in the region chain to display ''overset'' content. The final '''div''' element's [[apis/css-regions/Region/regionOverset|'''regionOverset''']] property returns '''overset'''. The named flow's [[apis/css-regions/NamedFlow/overset|'''overset''']] property likewise returns '''true'''.
|Code=<syntaxhighlight language="html">
<section class="layout">
  <div>
      	    <article class="content">
              <p>Content #1</p>
              <p>Content...
  </div>
  <div>
              ...#2</p>
  </div>
  <div>
              ...
  </div>
  <div>
              <p>Content #n</p>
  </div>
</section>

<!-- OVERSET CONTENT, DOES NOT DISPLAY:
              <p>Final Content</p>
      	     </article>
-->
</syntaxhighlight>
}}{{Single Example
|Language=HTML
|Description=''Scenario #3:'' In this example, there is ''not enough'' content to fill the region chain. The final '''div''' element's [[apis/css-regions/Region/regionOverset|'''regionOverset''']] property returns '''empty'''.
|Code=<syntaxhighlight language="html">
<section class="layout">
  <div>
      	    <article class="content">
              <p>Content #1</p>
              <p>Content...
  </div>
  <div>
              ...#2</p>
              ...
              <p>Content #n</p>
  </div>
  <div>
              <p>Final Content</p>
      	     </article>
  </div>
  <div>
              <!-- EMPTY REGION -->
  </div>
</section>
</syntaxhighlight>
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Regions Module Level 3
|URL=http://dev.w3.org/csswg/css3-regions/
|Status=W3C Editor's Draft
}}
}}
{{See_Also_Section
|Topic_clusters=Regions
|External_links=* W3C editor's draft: [http://dev.w3.org/csswg/css3-regions/ CSS Regions Module Level 3]
* Adobe Web Standards: [http://html.adobe.com/webstandards/cssregions CSS Regions]
* Adobe Developer's Network: [http://www.adobe.com/devnet/html5/articles/css3-regions.html CSS3 Regions: Rich page layout with HTML and CSS3]
* [http://adobe.github.com/web-platform/samples/css-regions Sample pages]
}}
{{Topics|CSS-Regions}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}