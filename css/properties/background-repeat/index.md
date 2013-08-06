{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Background-repeat defines if and how background images will be repeated after they have been sized and positioned}}
{{CSS Property
|Initial value=repeat
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=A list, each item consisting of two keywords, one per dimension
|Animatable=No
|CSS object model property=backgroundRepeat
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=<repeat-style>
|Description=Keyword(s) indicating the repeat pattern.

;<code>repeat</code>
:Default. In CSS2.1, the image is repeated horizontally and vertically. In CSS3, if two keywords are used, the image is repeated along the relevant axis.
;<code>no-repeat</code>
:The image is not repeated.
;<code>repeat-x</code>
:The image is repeated along the horizontal axis.
;<code>repeat-y</code>
:The image is repeated along the vertical axis.
;<code>round</code>
:The image is repeated as often as will fit into the background area, and is rescaled if necessary to make it fit a whole number of times. '''(CSS3)'''
;<code>space</code>
:The image is repeated as often as will fit into the background area a whole number of times, and is spaced out so that the first and last ones touch the edges. '''(CSS3)'''
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The following examples use the '''background-repeat''' attribute and the '''background-repeat''' property to specify whether the background image is tiled.

This example uses a call to an embedded (global) style sheet to tile the image.
|Code=&lt;STYLE&gt;
    .style1 { background-image:url(sphere.jpg);
        background-repeat:repeat }
    .style2 { background-image:url(sphere.jpeg);
        background-repeat:no-repeat }
&lt;/STYLE&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;SPAN onmouseover{{=}}"this.className{{=}}'style1'"
onmouseout{{=}}"this.className{{=}}'style2'" onclick{{=}}"this.className{{=}}''"&gt;
. . . &lt;/SPAN&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/background-repeat.htm
}}{{Single Example
|Language=CSS
|Description=This example shows how to use inline scripting to tile the image.
|Code=&lt;SPAN onmouseover{{=}}"this.style.backgroundImage{{=}}'url(sphere.jpeg)';
this.style.backgroundRepeat{{=}}'repeat'"&gt;
:
&lt;/SPAN&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/backgroundRepeat.htm
}}{{Single Example
|Language=CSS
|LiveURL=[https://developer.mozilla.org/en-US/docs/CSS/border-bottom-left-radius View MDN's examples]
}}
}}
{{Notes_Section
|Usage=In CSS2.1, only one keyword is permitted, affecting both the horizontal and vertical axes.

In CSS3, one or two keywords are permitted. One keyword affects both axes in the same way as CSS2.1 If two keywords are used, the first applies to the horizontal axis, and the second to the vertical axis.

If an element has multiple background images, the repeat pattern for each image can be set by assigning a comma-separated list of individual values. The values are applied to the background images in the same order as they are listed in the <code>background-image</code> property.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=All
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=All
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=All
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=All
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=All
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=CSS3 Syntax
|Chrome_supported=No
|Chrome_version=
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=10.5
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=All
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=All
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=All
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=All
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=All
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=All
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_version=All
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=All
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Chrome
|Version=All
|Note=The '''round''' and '''space''' keywords are treated as '''no-repeat'''.
}}{{Compatibility Notes Row
|Browser=Firefox
|Version=All
|Note=The '''round''' and '''space''' keywords are treated as '''repeat'''.
}}{{Compatibility Notes Row
|Browser=Safari
|Version=All.
|Note=The '''round''' and '''space''' keywords are treated as '''no-repeat'''.
}}
}}
{{See_Also_Section
|Topic_clusters=Background
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}