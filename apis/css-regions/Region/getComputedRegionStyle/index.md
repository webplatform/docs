{{Page_Title}}
{{Flags
|High-level issues=Stub
|Content=Incomplete, Examples Needed
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Returns styles calculated for an element as it appears within a region, including styles from [[css/atrules/@region|'''@region''']] rules applied to ranges within the element.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=element
|Data type=DOM Node
|Description=The element that contains the desired style settings, regardless of whether it currently appears within the region.
|Optional=No
}}{{Method Parameter
|Name=pseudoElementName
|Data type=String
|Description=The name of a CSS pseudo-element (such as "::before" or "::after") or a null value. Optional in WebKit-based browsers.
|Optional=Yes
}}
|Method_applies_to=apis/css-regions/Region
|Example_object_name=region
|Return_value_name=propValue
|Javascript_data_type=CSSStyleDeclaration
|Return_value_description=Returns styles calculated for an element as it appears within a region, including styles from [[css/atrules/@region|'''@region''']] rules applied to ranges within the element.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Check if the formatting of an element's property varies within a region chain
|Code=var flow = document.webkitGetNamedFlows()['sidebar'];
var regions = flow.getRegions();
var contents = flow.getContent();

// get a sample of pull-quote content
var pull = contents[0].querySelector('aside.pullquote')

// are there discrepancies in how the pull-quote's text
// would be colored throughout the region chain?
varies = regionsVaryCSS(regions, pull, 'color');

function regionsVaryCSS(regs, elem, prop) {
    var values = {};
    var value, style;
    var count = 0;
    for (var i = 0; i < regs.length; i++) {
        value = regs[i].getComputedRegionStyle(elem).getPropertyValue(prop);
        if (! values[value]) values[value] = 0;
        values[value]++;
    }
    for (key in values) if (values.hasOwnProperty(key)) count++;
    return count;
}
}}
}}
{{Notes_Section
|Usage=Behaves the same as [[css/cssom/methods/getComputedStyle|'''getComputedStyle()''']], but incorporates CSS formatting from [[css/atrules/@region|'''@region''']] rules that may apply to individual regions.
}}
{{Related_Specifications_Section
|Specifications=
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