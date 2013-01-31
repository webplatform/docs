{{Page_Title|background-position}}
{{Flags}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|<code>background-position</code> allows you to set the placement of a <code>background-image</code> on the element it is applied to. <code>background-position</code> generally takes two values, which set the horizontal and vertical position of the background image inside the element.}}
{{CSS Property
|Initial value=0 0
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=Pixel value equivalents
|Animatable=Yes
|CSS object model property=backgroundPosition
|Values={{CSS Property Value
|Data Type=20px 40px
|Description=Any standard CSS units are acceptable as <code>background-position</code> values: px, ems, rems, mm, cm etc. Note that unit values specify the distance the top left corner of the background image is away from the top left corner of the element. For more details on these units, read [[css/units/length|Length units]].

}}{{CSS Property Value
|Data Type=30% 15%
|Description=Percentages are acceptable for <code>background-position</code> values, and specify percentages of the overall width and height of the element in question. Note that percentage values specify the distance the top left corner of the background image is away from the top left corner of the element. For more details on percentages, read [[css/units/numeric|Numeric units]].
}}{{CSS Property Value
|Data Type=left top
|Description=<code>background-position</code> can also be expressed as keywords: left top, top, right top, left, center, right, left bottom, bottom, right bottom. These values do not relate specifically to the position of the top left hand corner of the background image, but rather the overall position of the background image inside the element. So for example, a value of <code>right top</code> will make the background image site flush to the top and right sides of the element it is applied to; the top left corner ''won't'' be positioned at the top right of the element!
}}{{CSS Property Value
|Data Type=30% top
|Description=A combination of different types of value (in this case, percentage then keyword) is allowed.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following examples use the '''background-position''' attribute and the '''background-position''' property to specify the position of a background image.

This example uses a call to an embedded (global) style sheet to move the sphere.
|Code=&lt;STYLE&gt;
    .style1 { background-position:top center }
    .style2 { background-position:bottom right }
&lt;/STYLE&gt;
&lt;/HEAD&gt;
&lt;BODY onload{{=}}"oSpan.className{{=}}'style1'"&gt;
&lt;SPAN STYLE{{=}}"font-size:14; width:250;" ID{{=}}"oSpan"
    onmouseover{{=}}"this.className{{=}}'style2'" onmouseout{{=}}"this.className{{=}}'style1'"&gt;
. . . &lt;/SPAN&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/background-position.htm
}}{{Single Example
|Description=This example uses an inline style to move the sphere.
|Code=&lt;SPAN onmouseover{{=}}"this.style.backgroundPosition{{=}}'bottom right'"&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/backgroundPosition.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
If only one value is set, that value applies to the horizontal coordinate, and the vertical is set to <code>50%</code>. If both values are set, the first value applies to the horizontal coordinate and the second value applies to the vertical.
Setting the values to <code>0% 0%</code> (initial value) positions the [[css/properties/background-image|'''background-image''']] to the upper left corner of the element's content block, which includes the padding.
Setting the background position using pixels positions the upper-left of the image at the specified x and y coordinates within the parent element. As the coordinates increase, the image moves to the right and down the visible area. By contrast, setting the background position with percentages uses a corresponding point on the image. At a position of <code>50% 50%</code> the image is effectively centered within the visible area.
This property can be set with the other background properties using the [[css/cssom/properties/background|'''background''']] composite property.
In Windows Internet Explorer 9, the background of a box can have multiple layers. The number of layers is determined by the number of comma-separated values in the [[css/properties/background-image|'''background-image''']] property. Each of the images is sized, positioned, and tiled according to the corresponding value in the other background properties ([[css/properties/background-attachment|'''background-attachment''']], [[css/properties/background-clip|'''background-clip''']], [[css/properties/background-origin|'''background-origin''']], '''background-position''', [[css/properties/background-repeat|'''background-repeat''']], and [[css/properties/background-size|'''background-size''']]). The first image in the list is the layer closest to the user, the next one is painted behind the first, and so on.
|Import_Notes====Syntax===
<code>'''background-position: ''''''[''' '''[''' percentage '''{{!}}''' length '''{{!}}''' left '''{{!}}''' center '''{{!}}''' right ''']''' '''[''' percentage '''{{!}}''' length '''{{!}}''' top '''{{!}}''' center '''{{!}}''' bottom ''']''''''?''' ''']''' '''{{!}}''' '''[''' '''[''' left '''{{!}}''' center '''{{!}}''' right ''']''' '''{{!}}{{!}}''' '''[''' top '''{{!}}''' center '''{{!}}''' bottom ''']''' ''']'''</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.3.6
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=Basic support
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.0 (1.7 or earlier)
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=4.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=3.5
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0 (85)
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=Multiple Backgrounds
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=3.6 (1.9.2)
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
|Safari_supported=Yes
|Safari_version=1.3 (312)
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=Four-value syntax (support for offsets from any edge)
|Chrome_supported=Yes
|Chrome_version=25
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=13.0 (13.0)
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
|Feature=Basic support
|Android_supported=Yes
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=1.0 (1)
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}{{Compatibility Table Mobile Row
|Feature=Multiple backgrounds
|Android_supported=Unknown
|Android_version=
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=1.0 (1.9.2)
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Unknown
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}{{Compatibility Table Mobile Row
|Feature=Four-value syntax (support for offsets from any edge)
|Android_supported=No
|Android_version=
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=25
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=13.0 (13.0)
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=9.0
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Background
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809 Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}