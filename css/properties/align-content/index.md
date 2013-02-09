{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name|CSS Flexible Box Layout Module}}
{{Summary_Section|The ‘align-content’ property aligns a flex container's lines within the flex container when there is extra space in the cross-axis, similar to how ‘justify-content’ aligns individual items within the main-axis. Note, this property has no effect when the flexbox has only a single line. Values have the following meanings:}}
{{CSS Property
|Initial value=stretch
|Applies to=multi-line flex containers
|Inherited=No
|Media=visual
|Computed value=specified value
|Animatable=No
|CSS object model property=alignContent
|Values={{CSS Property Value
|Data Type=flex-start
|Description=Lines are packed toward the start of the flex container. The cross-start edge of the first line in the flex container is placed flush with the cross-start edge of the flex container, and each subsequent line is placed flush with the preceding line.
}}{{CSS Property Value
|Data Type=flex-end
|Description=Lines are packed toward the end of the flex container. The cross-end edge of the last line is placed flush with the cross-end edge of the flex container, and each preceding line is placed flush with the subsequent line.
}}{{CSS Property Value
|Data Type=center
|Description=Lines are packed toward the center of the flex container. The lines in the flex container are placed flush with each other and aligned in the center of the flex container, with equal amounts of empty space between the cross-start content edge of the flex container and the first line in the flex container, and between the cross-end content edge of the flex container and the last line in the flex container. (If the leftover free-space is negative, the lines will overflow equally in both directions.)
}}{{CSS Property Value
|Data Type=space-between
|Description=Lines are evenly distributed in the flex container. If the leftover free-space is negative this value is identical to ‘flex-start’. Otherwise, the cross-start edge of the first line in the flex container is placed flush with the cross-start content edge of the flex container, the cross-end edge of the last line in the flex container is placed flush with the cross-end content edge of the flex container, and the remaining lines in the flex container are distributed so that the empty space between any two adjacent lines is the same.
}}{{CSS Property Value
|Data Type=space-around
|Description=Lines are evenly distributed in the flex container, with half-size spaces on either end. If the leftover free-space is negative this value is identical to ‘center’. Otherwise, the lines in the flex container are distributed such that the empty space between any two adjacent lines is the same, and the empty space before the first and after the last lines in the flex container are half the size of the other empty spaces.
}}{{CSS Property Value
|Data Type=stretch
|Description=Lines stretch to take up the remaining space. If the leftover free-space is negative, this value is identical to ‘flex-start’. Otherwise, the free-space is split equally between all of the lines, increasing their cross size.
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=[file:aligncontent.svg]
(Image from [http://www.w3.org/TR/css3-flexbox/#align-content-property CSS Flexible Box Layout Module])
|Notes=Only flex containers with multiple lines ever have free space in the cross-axis for lines to be aligned in, because in a flex container with a single line the sole line automatically stretches to fill the space.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Flexible Box Layout Module
|URL=http://www.w3.org/TR/css3-flexbox/#align-content-property
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