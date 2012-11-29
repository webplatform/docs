{{Page_Title|regionlayoutupdate event}}
{{Flags}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Fires on the  [[css/cssom/NamedFlow|'''NamedFlow''']] object when there is a change in how content flows through a region chain.}}
{{Event
|Event_applies_to=apis/css-regions/NamedFlow
|Content=Fires on the  [[css/cssom/NamedFlow|'''NamedFlow''']] object when there is a change in how content flows through a region chain.
|Interface=TBD
|Target=dom/Element
|Default_action=TBD
|Synchronous=TBD
|Bubbles=TBD
|Cancelable=TBD
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=document.getNamedFlows()['main'].addEventListener('regionlayoutupdate', modifyFlow);

// dispatches functions to add/delete regions based on changes to how
// content flows through a region chain:

function modifyFlow(e) {
    var flow = e.target;
    if (flow.overset) {
      	appendRegion(flow.name); // custom function
    }
    else if (flow.firstEmptyRegionIndex !== -1)	{
        trimRegions(flow.name); // custom function
    }
}
}}
}}
{{Notes_Section
|Notes=The event fires when linebreaks shift in any way within the region chain, even without changing the number of regions that are filled with content and changing any region's [[apis/css-regions/Region/regionOverset|'''regionOverset''']] state. More specifically, the event fires when any region's [[apis/css-regions/Region/getRegionFlowRanges|collection of DOM Range fragments]] changes their dimensions or offsets.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Regions Module Level 3
|URL=http://dev.w3.org/csswg/css3-regions/
}}
}}
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