{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name|CSS Flexible Box Layout Module}}
{{Summary_Section|'align-items' sets the default alignment for all of the flex container's items, including anonymous flex items.}}
{{CSS Property
|Initial value=stretch
|Applies to=flex containers
|Inherited=No
|Media=visual
|Computed value=specified value
|Animatable=No
|Values={{CSS Property Value
|Data Type=flex-start
|Description=The cross-start margin edge of the flex item is placed flush with the cross-start edge of the line.
}}{{CSS Property Value
|Data Type=flex-end
|Description=The cross-end margin edge of the flex item is placed flush with the cross-end edge of the line.
}}{{CSS Property Value
|Data Type=center
|Description=The flex item's margin box is centered in the cross axis within the line. (If the cross size of the flex line is less than that of the flex item, it will overflow equally in both directions.)
}}{{CSS Property Value
|Data Type=baseline
|Description=If the flex item's inline axis is the same as the cross axis, this value is identical to 'flex-start'.

Otherwise, it participates in baseline alignment: all participating flex items on the line are aligned such that their baselines align, and the item with the largest distance between its baseline and its cross-start margin edge is placed flush against the cross-start edge of the line.
}}{{CSS Property Value
|Data Type=stretch
|Description=If the cross size property of the flex item is 'auto', its used value is the length necessary to make the cross size of the item's margin box as close to the same size as the line as possible, while still respecting the constraints imposed by 'min/max-width/height'.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Displaying children centered horizontally
|Code=.list {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.list div {
  flex: 1;
}
|LiveURL=http://dabblet.com/gist/4745348
}}{{Single Example
|Language=CSS
|Description=Displaying children centered vertically
|Code=.list {
  display: flex;
  flex-direction: row;
  align-items: center;
  height: 100px;
}

.list div {
  flex: 1;
}
|LiveURL=http://dabblet.com/gist/4745341
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Flexible Box Layout Module
|URL=http://www.w3.org/TR/css3-flexbox/#align-items-property
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