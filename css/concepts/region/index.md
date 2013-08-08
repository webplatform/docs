{{Page_Title|regions}}
{{Flags
|Checked_Out=No
}}
{{API_Name}}
{{Summary_Section|The ''CSS Regions'' feature allows content to flow dynamically through a series of presentational block elements, known as [[css/concepts/region|''regions'']], allowing for complex magazine-style layouts.}}
{{Concept_Page

|Content=

Two CSS properties make it work. The
[[css/properties/flow-into|'''flow-into''']] property diverts content
into a [[css/concepts/named_flow|''named flow'']]. The
[[css/properties/flow-from|'''flow-from''']] property threads that
flow's content through a dynamic series of
[[css/concepts/region|''region'']] elements, collectively known as a
[[css/concepts/region_chain|''region chain'']].  The feature allows
content to thread through a document's regions, magazine-style.
Regions can be positioned using various other CSS techniques, such as
[[tutorials/flexbox|flexible boxes]],
[[tutorials/CSS_absolute_and_fixed_positioning|fixed positioning]],
[[tutorials/floats_and_clearing|floats]], or grids.

Assigning [[css/properties/flow-from|'''flow-from''']] to a block
element turns it into a region. As long as it serves as a region, any
of its content is obscured by content diverted from other elements
whose [[css/properties/flow-into|'''flow-into''']] property specifies
the same [[css/concepts/named_flow|''named flow'']]. (If there is no
corresponding [[css/properties/flow-into|'''flow-into''']] content,
the region displays nothing.)

Use the [[apis/css-regions/Region|'''Region''']] interface to
programatically access each region within a chain, and the
[[apis/css-regions/NamedFlow|'''NamedFlow''']] interface to access the
overall content that flows within the chain.

}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Usage=
|Notes=
}}
{{Related_Specifications_Section
|Specifications=
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