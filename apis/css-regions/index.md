{{Page_Title|CSS Regions API}}
{{Flags
|High-level issues=Stub
|Content=Incomplete, Examples Needed
|Editorial notes=test case to migrate to /apis/ structure
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Programmatic interface to content that flows through a series of chained ''region'' elements, as specified by [[css/properties/flow-into|'''flow-into''']] and [[css/properties/flow-from|'''flow-from''']] CSS properties.}}
{{API_Listing
|Use_page_title=No
|List_all_subpages=No
}}
{{Notes_Section
|Usage=CSS Regions are defined by
[[css/properties/flow-into|'''flow-into''']] and
[[css/properties/flow-from|'''flow-from''']] CSS properties.  The
[[css/properties/flow-into|'''flow-into''']] property diverts content
into a ''named flow'', while the
[[css/properties/flow-from|'''flow-from''']] property pours that
flow's content through a dynamic chain of ''region'' elements.  The
feature allows content to follow a path through arbitrarily placed
magazine-style layout elements.

Two interfaces allow programmatic access to the CSS Regions feature:

* The [[apis/css-regions/NamedFlow|'''NamedFlow''']] interface provides access to the content defined as [[css/properties/flow-into|'''flow-into''']], and the series of layout regions defined as [[css/properties/flow-from|'''flow-from''']].  Use the [[dom/apis/document/getNamedFlows|getNamedFlows()]] method to access these flows.

* The [[apis/css-regions/Region|'''Region''']] interface provides information on each region within the chain.
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