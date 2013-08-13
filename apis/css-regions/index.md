{{Page_Title|CSS Regions API}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Programmatic interface to [[css/concepts/named_flow|content that flows]] through a series of [[css/concepts/region_chain|chained]] [[css/concepts/region|''region'']] elements.}}
{{API_Listing|Query=[[Category:CSS-Regions]][[Category:API_Objects]]
|Use_page_title=Yes
|List_all_subpages=No
}}
{{Concept_Listing
|Use_page_title=No
|List_all_subpages=No
}}
{{Notes_Section
|Usage=CSS Regions are defined by two CSS properties.  The
[[css/properties/flow-into|'''flow-into''']] property diverts content
into a [[css/concepts/named_flow|''named flow'']], and the
[[css/properties/flow-from|'''flow-from''']] property pours that
flow's content through a dynamic [[css/concepts/region_chain|chain]]
of [[css/concepts/region|''region'']] elements.  The feature allows
content to follow a path through arbitrarily placed magazine-style
layout elements. Use as follows:

* The [[apis/css-regions/Document/getNamedFlows|'''getNamedFlows()''']] method, available via the [[dom/apis/document|'''Document''']] interface, retrieves all of a document's named flows as a [[apis/css-regions/NamedFlowCollection|'''NamedFlowCollection''']].

* Iterate over the [[apis/css-regions/NamedFlowCollection|'''NamedFlowCollection''']] as an array, or call [[apis/css-regions/NamedFlowCollection/namedItem|'''namedItem''']] on it to access each [[apis/css-regions/NamedFlow|'''NamedFlow''']] by its name.

* The [[apis/css-regions/NamedFlow|'''NamedFlow''']] interface provides access to the content defined as [[css/properties/flow-into|'''flow-into''']], and the series of layout regions defined as [[css/properties/flow-from|'''flow-from''']]. Use it to check if the amount of content matches the allotted set of regions in which it appears.

* The [[apis/css-regions/Region|'''Region''']] interface provides information on each region within the chain, and allows access to [[css/concept/fragment|fragments]] of content that dynamically appear there.

For an overview of CSS Regions, see [[tutorials/css-regions|Using CSS Regions to flow content through a layout]].
}}
{{See_Also_Section
|Topic_clusters=Regions
|External_links=* W3C editor's draft: [http://dev.w3.org/csswg/css3-regions/ CSS Regions Module Level 3]
* Adobe Web Standards: [http://html.adobe.com/webstandards/cssregions CSS Regions]
* Adobe Developer's Network: [http://www.adobe.com/devnet/html5/articles/css3-regions.html CSS3 Regions: Rich page layout with HTML and CSS3]
* [http://adobe.github.com/web-platform/samples/css-regions Sample pages]
}}
{{Topics|API, CSS-Regions}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}