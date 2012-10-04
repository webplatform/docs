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
|Values={{CSS_Property_Value|Data Type=repeat |Description=Default. Image is repeated horizontally and vertically.}}
{{CSS_Property_Value|Data Type=no-repeat |Description=Image is not repeated.}}
{{CSS_Property_Value|Data Type=repeat-x |Description=Image is repeated horizontally.}}
{{CSS_Property_Value|Data Type=repeat-y |Description=Image is repeated vertically.}}
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following examples use the '''background-repeat''' attribute and the '''background-repeat''' property to specify whether the background image is tiled.

This example uses a call to an embedded (global) style sheet to tile the image.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/background-repeat.htm
|Code=
&lt;STYLE&gt;
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
}}
{{Single_Example
|Description=This example shows how to use inline scripting to tile the image.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/backgroundRepeat.htm
|Code=
&lt;SPAN onmouseover{{=}}"this.style.backgroundImage{{=}}'url(sphere.jpeg)';
this.style.backgroundRepeat{{=}}'repeat'"&gt;
:
&lt;/SPAN&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''repeat-x''' and '''repeat-y''' values make the image repeat horizontally and vertically, respectively, creating a single band of images from one side to the other.
This property can be set with other background properties by using the [[css/cssom/properties/background|'''background''']] composite property.
In Windows Internet Explorer 9, the background of a box can have multiple layers. The number of layers is determined by the number of comma-separated values in the [[css/properties/background-image|'''background-image''']] property. Each of the images is sized, positioned, and tiled according to the corresponding value in the other background properties ([[css/properties/background-attachment|'''background-attachment''']], [[css/properties/background-clip|'''background-clip''']], [[css/properties/background-origin|'''background-origin''']], [[css/properties/background-position|'''background-position''']], '''background-repeat''', and [[css/properties/background-size|'''background-size''']]). The first image in the list is the layer closest to the user, the next one is painted behind the first, and so on.
|Import_Notes=
===Syntax===
<code>'''background-repeat: '''repeat '''{{!}}''' repeat-x '''{{!}}''' repeat-y '''{{!}}''' no-repeat</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.3.4


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