{{Page_Title|overset content}}
{{Flags
|Checked_Out=No
}}
{{API_Name}}
{{Summary_Section|Refers to a situation in which the final [[css/concepts/region|''region'']] of a [[css/concepts/region_chain|''region chain'']] is unable to fully display remaining content of a [[css/concepts/named_flow|''named flow'']].}}
{{Concept_Page
|Content=The 'CSS Regions' feature allows content to flow dynamically through
a series of presentational block elements, known as
[[css/concepts/region|''regions'']], allowing for complex
magazine-style layouts. This [[css/concepts/region_chain|'region
chain']] may not have enough room to accommodate all the content.  In
that case, the final region is in an
[[css/concepts/overset|''overset'']] state, as is the
[[css/concepts/named_flow|''named flow'']] that contains all the
content.

Depending on its
[[css/properties/region-fragment|'''region-fragment''']] property, the
final [[css/concepts/region|region's]] content may appear as a
[[css/concepts/fragment|''fragment'']], breaking cleanly as if there
were subsequent regions in the chain into which content could flow.
Otherwise it may simply 'overflow' the final element, either
clipping, spilling or scrolling past the element's dimensions as set
by the [[css/properties/overflow|'''overflow''']] property.

There are two ways to programatically detect overset state:

* From the content side, if the [[css/concepts/named_flow|named flow's]] [[apis/css-regions/NamedFlow/overset|'''overset''']] property is '''true''', it means that it doesn't fully display within the [[css/concepts/region_chain|region chain]], or that it has not been placed within any [[css/concepts/region|regions]].

* On the presentation side, if the final region element's [[apis/css-regions/Region/regionOverset|'''regionOverset''']] property is '''overset''', some of its content can flow into another region if available.

For an overview of CSS Regions, see [[tutorials/css-regions|Using CSS Regions to flow content through a layout]].
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}