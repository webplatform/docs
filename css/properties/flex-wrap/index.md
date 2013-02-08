{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name|CSS Flexible Box Layout Module}}
{{Summary_Section|The ‘flex-wrap’ property controls whether the flex container is single-line or multi-line, and the direction of the cross-axis, which determines the direction new lines are stacked in. }}
{{CSS Property
|Initial value=nowrap
|Applies to=flex containers
|Inherited=No
|Computed value=specified value
|Animatable=No
|CSS object model property=flexWrap
|Values={{CSS Property Value
|Data Type=nowrap
|Description=The flex container is single-line. The cross-start direction is equivalent to either the start or before/head direction of the current writing mode, whichever is in the cross axis, and the cross-end direction is the opposite direction of cross-start. 
}}{{CSS Property Value
|Data Type=wrap
|Description=The flex container is multi-line. The cross-start direction is equivalent to either the start or before/head direction of the current writing mode, whichever is in the cross axis, and the cross-end direction is the opposite direction of cross-start. 
}}{{CSS Property Value
|Data Type=wrap-reverse
|Description=Same as ‘wrap’, except the cross-start and cross-end directions are swapped. 
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Displaying children in a non-wrapping row
|Code=.list {
  display: flex;
  flex-wrap: nowrap;
}

.list div {
  flex: 1;
}
|LiveURL=http://dabblet.com/gist/4740662
}}{{Single Example
|Language=CSS
|Description=Displaying children in a row wrapping to the next line
|Code=.list {
  display: flex;
  flex-wrap: wrap;
}

.list div {
  flex: 1;
}
|LiveURL=http://dabblet.com/gist/4740667
}}{{Single Example
|Language=CSS
|Description=Displaying children in a row wrapping to the previous line
|Code=.list {
  display: flex;
  flex-wrap: wrap-reverse;
}

.list div {
  flex: 1;
}
|LiveURL=http://dabblet.com/gist/4740670
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Flexible Box Layout Module
|URL=http://www.w3.org/TR/css3-flexbox/#flex-wrap-property
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