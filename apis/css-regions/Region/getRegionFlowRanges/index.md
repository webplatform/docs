{{Page_Title}}
{{Flags
|High-level issues=Stub, Needs Topics
|Content=Incomplete, Examples Needed
|Editorial notes=references DOM Range API, for which there's no apparent doc available
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Returns a series of '''Range''' objects that represent the fragments of DOM content that currently flow into the region.}}
{{API_Object_Method
|Parameters=
|Method_applies_to=apis/css-regions/Region
|Example_object_name=region
|Return_value_name=ranges
|Javascript_data_type=function
|Return_value_description=Returns a series of '''Range''' objects that represent the fragments of DOM content that currently flow into the region.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Check a region for interruptions in source content:
|Code=// get flow                                                                                                                     
var flow = document.webkitGetNamedFlows()['main'];

// get second region that displays content                                                                                      
var region = flow.getRegions()[1];

// how many content fragments display there?                                                                                    
var ranges = region.getRegionFlowRanges();

// perhaps do something to fix layout if content has been interrupted:                                                          
if (ranges.length > 1) {
    adjustlayout(region) // custom function                                                                                     
}

}}
}}
{{Notes_Section
|Usage=Regions may display more than one range, because more than one element may specify [[css/properties/flow-into|'''flow-into''']] to contribute to a flow, and the boundary between those content elements may fall within a region. Also, any content element's nested elements can be diverted to a different named flow, thus interrupting the original sequence of content. (See [[css/properties/flow-into|'''flow-into''']] for more details.)

By default, calling '''getRegionFlowRanges()''' on an overflowing region at the end of a chain (one whose [[apis/css-regions/Region/regionOverset|'''regionOverset''']] is '''overset''') returns fragments representing all remaining content that may [[css/properties/overflow|'''overflow''']] out of view.  If the region's [[css/properties/region-fragment|'''region-fragment''']] property is set to '''break''', it returns only those fragments of content that fit neatly within the region.

If the region is too small to display the content, it returns a single collapsed range.

Calling it on an empty region (one whose [[apis/css-regions/Region/regionOverset|'''regionOverset''']] is '''empty''') returns an empty list.

Calling it on an element that is no longer a region (when its [[css/properties/flow-from|'''flow-from''']] property reverts to '''none''') returns '''null'''. The following tests whether the block element currently serves as a region:

 isRegion = (element.getRegionFlowRanges() !== null);
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