{{Page_Title}}
{{Flags
|High-level issues=Stub
|Content=Incomplete, Examples Needed
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Represents content to flow among various block ''region''
elements. The '''NamedFlow''' interface allows access to both the
content of the flow and the series of regions in which it displays,
and helps determine if the content exceeds or falls short of the
number of regions necessary to display it.
}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Generic event handler dispatches functions to add or delete regions based on changes to how content flows through a region chain:
|Code=document.getNamedFlows()['main'].addEventListener('regionlayoutupdate', modifyFlow);
document.getNamedFlows()['figures'].addEventListener('regionlayoutupdate', modifyFlow);

function modifyFlow(e) {
    var flow = e.target;
    // does content exceed available regions?
    if (flow.overset) {
      	appendRegion(flow.name);
    }
    // ...or does insufficient content leave some regions empty?
    else if (flow.firstEmptyRegionIndex !== -1)	{
        trimRegions(flow.name);
    }
}
}}{{Single Example
|Language=JavaScript
|Code=// 2do
}}
}}
{{Notes_Section
|Usage=Specifying an identifier for any element's
[[css/properties/flow-into|'''flow-into''']] CSS property diverts its
content to a '''NamedFlow''' object,
whose '''name''' corresponds to the property's value. 
Other elements that specify the same identifier as their
[[css/properties/flow-from|'''flow-from''']] property serve as a chain
of ''regions'' that dynamically display the content.  (The
'''NamedFlow''' object is still available with NULL content if those
properties are later removed.)

Use the [[dom/apis/document/getNamedFlows|'''getNamedFlows''']] method to gather named flows from a document.
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
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}