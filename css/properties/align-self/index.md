{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Allows the default alignment to be overridden for individual flex items.}}
{{CSS Property
|Initial value=auto
|Applies to=flex items
|Inherited=No
|Media=visual
|Computed value='''auto''' computes to parent's '''align-items''', or '''stretch''' if the element has no parent; otherwise as specified
|Animatable=No
|CSS object model property=alignSelf
|Values={{CSS Property Value
|Data Type=auto
|Description=Computes to the value of [[css/properties/align-items|align-items]] on the element's parent, or '''stretch''' if the element has no parent.
}}{{CSS Property Value
|Data Type=flext-start
|Description=The cross-start margin edge of the flex item is placed flush with the cross-start edge of the line.
}}{{CSS Property Value
|Data Type=flex-end
|Description=The cross-end margin edge of the flex item is placed flush with the cross-end edge of the line.
}}{{CSS Property Value
|Data Type=center
|Description=The flex item's margin box is centered in the cross axis within the line. (If the cross size of the flex line is less than that of the flex item, it will overflow equally in both directions.)
}}{{CSS Property Value
|Data Type=baseline
|Description=If the flex item's inline axis is the same as the cross axis, this value is identical to '''flex-start'''.

Otherwise, it participates in baseline alignment: all participating flex items on the line are aligned such that their baselines align, and the item with the largest distance between its baseline and its cross-start margin edge is placed flush against the cross-start edge of the line.
}}{{CSS Property Value
|Data Type=stretch
|Description=If the cross size property of the flex item is '''auto''', its used value is the length necessary to make the cross size of the item's margin box as close to the same size as the line as possible, while still respecting the constraints imposed by [[css/properties/min-height|min-height]]/[[css/properties/min-width|min-width]]/[[css/properties/max-height|max-height]]/[[css/properties/max-width|max-width]]. Note: that if the flex container's height is constrained the stretch value may cause the contents of the flex item to overflow the item.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Displaying children with custom alignment.
|Code=.list {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.list div {
  flex: 1;
}

.list .second {
  align-self: flex-end;
}
|LiveURL=http://code.webplatform.org/gist/4745364
}}
}}
{{Notes_Section
|Notes=* This property will have no effect if the flex-item's cross axis margins are set to auto.
* This property was named '''flex-item-align''' in older drafts.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Flexible Box Layout Module
|URL=http://www.w3.org/TR/css3-flexbox/#align-self-property
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
|Topic_clusters=Flexbox
|External_links=Also, check out the following live demo sites:
* [http://demo.agektmr.com/flexbox/ Flexbox Playground]
* [http://the-echoplex.net/flexyboxes Flexy Boxes]
}}
{{Topics|Flexbox}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}