{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name|CSS Flexible Box Layout Module}}
{{Summary_Section|The ‘flex-flow’ property is a shorthand for setting the ‘flex-direction’ and ‘flex-wrap’ properties, which together define the flex container's main and cross axes. }}
{{CSS Property
|Initial value=See individual properties: [[css/properties/flex-direction|flex-direction]] [[css/properties/flex-wrap|flex-wrap]]
|Applies to=flex containers
|Inherited=No
|Media=visual
|Computed value=See individual properties: [[css/properties/flex-direction|flex-direction]] [[css/properties/flex-wrap|flex-wrap]]
|Animatable=No
|CSS object model property=flexFlow
|Values={{CSS Property Value
|Data Type=<flex-direction> <flex-wrap>
|Description=See individual properties: [[css/properties/flex-direction|flex-direction]] [[css/properties/flex-wrap|flex-wrap]]
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Displaying children in a row wrapping to the next line
|Code=.list {
  display: flex;
  flex-flow: row wrap;
}

.list div {
  flex: 1;
}
|LiveURL=http://dabblet.com/gist/4740728
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Flexible Box Layout Module
|URL=http://www.w3.org/TR/css3-flexbox/#flex-flow-property
|Status=Candidate Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables={{Imported Compatibility Table
|Page=http://caniuse.com/#flexbox
}}
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=CSS Layout, Flexbox
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}