{{Page_Title|named flow}}
{{Flags
|Checked_Out=No
}}
{{API_Name}}
{{Summary_Section|An object that contains content diverted from one set of elements, which can then be threaded through another series of [[css/concepts/region|''regions'']] that display the content.}}
{{Concept_Page

|Content=The 'CSS Regions' feature allows content to flow
dynamically through a series of presentational block elements, known
as [[css/concepts/region|''regions'']], allowing for complex
magazine-style layouts.

Two CSS properties make this feature work. The
[[css/properties/flow-into|'''flow-into''']] property diverts content
into a [[css/concepts/named_flow|''named flow'']]. The
[[css/properties/flow-from|'''flow-from''']] property threads that
flow's content through a dynamic series of
[[css/concepts/region|''region'']] elements, collectively known as a
[[css/concepts/region_chain|''region chain'']].

The following shows a complex layout featuring a series of regions,
with a named flow's content threading through regions ''1'' through
''4'', which form a chain. A separate named flow is assigned to the
single-element region chain labeled ''A'':

[[Image:regions.png|400px]]

There can be more than one [[css/concepts/named_flow|named flow]] in a
document. Each named flow can accumulate content from more than one
element via the [[css/properties/flow-into|'''flow-into''']] property,
but they do so according to the order in which they appear in the
document.  Use the [[apis/css-regions/NamedFlow|'''NamedFlow''']]
interface to programatically access the named flow's content.

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
|Specifications={{Related Specification
|Name=CSS Regions Module Level 3
|URL=http://dev.w3.org/csswg/css3-regions/
|Status=W3C Editor's Draft
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