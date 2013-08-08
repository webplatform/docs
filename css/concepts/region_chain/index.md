{{Page_Title|region chains}}
{{Flags
|Checked_Out=No
}}
{{API_Name}}
{{Summary_Section|A series of [[css/concepts/region|''regions'']] that display the contents of a [[css/concepts/named_flow|''named flow'']].
}}
{{Concept_Page
|Content=The 'CSS Regions' feature allows content to flow dynamically
through a series of presentational block elements, known as
[[css/concepts/region|''regions'']], allowing for complex magazine-style
layouts. Each available [[css/concepts/named_flow|''named flow'']],
identified by content elements'
[[css/properties/flow-into|'''flow-into''']] property, threads through
a [[css/concepts/region_chain|chain]] of block elements whose
[[css/properties/flow-from|'''flow-from''']] property matches.
Regardless of how each region is positioned, content threads through
the [[css/concepts/region_chain|region chain]] in 'DOM order', the
order in which regions are declared within the HTML document.

The following shows a complex layout featuring a series of regions,
with a named flow's content threading through regions ''1'' through
''4'', which form a chain. A separate named flow is assigned to the
single-element region chain labeled ''A'':

[[Image:regions.png|400px]]

A [[css/concepts/region_chain|region chain]] may have either not
enough or too many elements to neatly display a
[[css/concepts/named_flow|named flow]]'s content.  The
[[apis/css-regions/NamedFlow|'''NamedFlow''']] interface's
[[apis/css-regions/NamedFlow/overset|'''overset''']] property allows
you to programatically identify the latter
[[css/concepts/overset|''overset'']] case for a body of content.  The
[[apis/css-regions/Region|'''Region''']] interface's
[[apis/css-regions/Region/regionOverset|'''regionOverset''']] property
allows you to identify both cases, '''empty''' or '''overset''', by
examining regions within the chain, which are available via the named
flow's [[apis/css-regions/NamedFlow/getRegions|'''getRegions()''']]
method.

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