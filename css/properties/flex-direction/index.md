{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name|CSS Flexible Box Layout Module}}
{{Summary_Section|The ‘flex-direction’ property specifies how flex items are placed in the flex container, by setting the direction of the flex container's main axis. This determines the direction that flex items are laid out in.}}
{{CSS Property
|Initial value=row
|Applies to=flex containers
|Inherited=No
|Media=visual
|Computed value=specified value
|Animatable=No
|CSS object model property=flexDirection
|Values={{CSS Property Value
|Data Type=row
|Description=The flex container's main axis has the same orientation as the inline axis of the current writing mode. The main-start and main-end directions are equivalent to the start and end directions, respectively, of the current writing mode.
}}{{CSS Property Value
|Data Type=row-reverse
|Description=Same as ‘row’, except the main-start and main-end directions are swapped.
}}{{CSS Property Value
|Data Type=column
|Description=The flex container's main axis has the same orientation as the block axis of the current writing mode. The main-start and main-end directions are equivalent to the before/head and after/foot directions, respectively, of the current writing mode.
}}{{CSS Property Value
|Data Type=column-reverse
|Description=Same as ‘column’, except the main-start and main-end directions are swapped.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Displaying children in a row
|Code=.list {
  display: flex;
  flex-direction: row;
}

.list div {
  flex: 1;
}
|LiveURL=http://dabblet.com/gist/4740224
}}{{Single Example
|Language=CSS
|Description=Displaying children in a row in reversed order
|Code=.list {
  display: flex;
  flex-direction: row-reverse;
}

.list div {
  flex: 1;
}
|LiveURL=http://dabblet.com/gist/4740260
}}{{Single Example
|Language=CSS
|Description=Displaying children in a column
|Code=.list {
  display: flex;
  flex-direction: column;
}

.list div {
  flex: 1;
}
|LiveURL=http://dabblet.com/gist/4740271
}}{{Single Example
|Language=CSS
|Description=Displaying children in a column in reversed order
|Code=.list {
  display: flex;
  flex-direction: column-reverse;
}

.list div {
  flex: 1;
}
|LiveURL=http://dabblet.com/gist/4740277
}}
}}
{{Notes_Section
|Notes=The reverse values do not reverse box ordering; like ‘writing-mode’ and ‘direction’, they only change the direction of flow. Painting order, speech order, and sequential navigation orders are not affected.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Flexible Box Layout Module
|URL=http://www.w3.org/TR/css3-flexbox/#flex-direction
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
|Manual_links=* http://www.w3.org/TR/css3-flexbox/#flex-direction
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}