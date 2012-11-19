{{Page_Title}}
{{Flags
|High-level issues=Stub
|Content=Incomplete, Examples Needed
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Returns styles calculated for the region, including styles from [[css/atrules/@region|'''@region''']] rules applied to ranges.}}
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
|Return_value_name=stylesheet
|Javascript_data_type=CSSStyleDeclaration
|Return_value_description=Returns styles calculated for the region, including styles from [[css/atrules/@region|'''@region''']] rules applied to ranges.
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

// are there discrepancies in how text would be colored
// throughout the chain?
varies = regionsVaryCSS(regions, pull, 'color');

function regionsVaryCSS(regs, elem, prop) {
    var values = {};
    var value, style;
    var count = 0;
    for (var i = 0; i < regs.length; i++) {
        value = regs[i].getComputedRegionStyle(elem).getPropertyValue(prop);
        values[value] || values[value] = 0;
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
|Desktop_rows=
|Mobile_rows=
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