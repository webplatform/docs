{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Returns the integer index of the first empty element within a region chain. Returns -1 if the content fits within the region chain or if it exceeds available space.}}
{{API_Object_Property
|Property_applies_to=apis/css-regions/NamedFlow
|Read_only=Yes
|Example_object_name=flow
|Return_value_name=index
|Javascript_data_type=Number
|Return_value_description=Returns the integer index of the first empty element within a region chain. Returns -1 if the content fits within the region chain or if it exceeds available space.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=trimRegions('mainFlow');

// deletes any empty regions from the end of a flow:
function trimRegions(flowName) {
    var flow = document.getNamedFlows()[flowName];
    var index = flow.firstEmptyRegionIndex;
    var regions = flow.getRegions();
    if (index == -1) return(false); // no empty regions?
    // remove first empty region & all thereafter:
    for (var i = index; i < regions.length; i++) {
        regions[i].parentNode.removeChild(regions[i]);
    }
    return(true);
}
}}
}}
{{Notes_Section
|Usage=The '''firstEmptyRegionIndex''' is the index of the first region
within the flow's [[css/cssom/NamedFlow/getRegions|getRegions]] whose
[[css/cssom/Region/regionOverset|regionOverset]] is '''empty'''.  If
all are set to '''fit''' or '''overset''', or if no regions are
associated with the flow, the '''firstEmptyRegionIndex''' returns -1.
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