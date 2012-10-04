{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_Property
|Applies to=All elements
|Media=visual
|Inherited=No
|Initial value=
|Values={{CSS_Property_Value|Data Type=none |Description=Default. Color of the next parent through which the background is visible.}}
{{CSS_Property_Value|Data Type=url |Description=Location of the background image(s), where <code>sUrl</code> is an absolute or relative URL.}}
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following examples use the '''background-image''' attribute and the '''background-image''' property to specify the background's image.

This example uses a call to an embedded (global) style sheet to show and hide the background image.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/background-image.htm
|Code=
&lt;style type{{=}}"text/css"&gt;
.setUrl {
    background-image: url(sphere.jpg);
}
.loseUrl {
    background-image: url(none);
}
&lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;span style{{=}}"font-size: 14px" onmouseover{{=}}"this.className{{=}}'setUrl'" onmouseout{{=}}"this.className{{=}}'loseUrl'"&gt;
. . . &lt;/span&gt;
}}
{{Single_Example
|Description=This example uses inline scripting to show and hide the background image.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/backgroundImage.htm
|Code=
&lt;span onmouseover{{=}}"this.style.backgroundImage{{=}}'url(sphere.jpeg)'"&gt;
. . . &lt;/span&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The URL identifies the image file. When setting a background image, you can set a background color to use when the image is unavailable. When the image is available, it overlays the background color.
This property can be set with other background properties by using the [[css/cssom/properties/background|'''background''']] composite property.
Microsoft Internet Explorer 3.0 supports the '''background-image''' attribute, but only when it's set through the [[css/cssom/properties/background|'''background''']] attribute.
In Windows Internet Explorer 9, the background of a box can have multiple layers. The number of layers is determined by the number of comma-separated values in the '''background-image''' property. Each of the images is sized, positioned, and tiled according to the corresponding value in the other background properties ([[css/properties/background-attachment|'''background-attachment''']], [[css/properties/background-clip|'''background-clip''']], [[css/properties/background-origin|'''background-origin''']], [[css/properties/background-position|'''background-position''']], [[css/properties/background-repeat|'''background-repeat''']], and [[css/properties/background-size|'''background-size''']]). The first image in the list is the layer closest to the user, the next one is painted behind the first, and so on.
|Import_Notes=
===Syntax===
<code>'''background-image: '''url '''{{!}}''' none</code>
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
|Topic_clusters=Background
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}