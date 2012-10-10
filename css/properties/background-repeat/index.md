{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Defines how background images will be repeated.}}
{{CSS Property
|Applies to=All elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=repeat
|Description=Default. Image is repeated horizontally and vertically.
}}{{CSS Property Value
|Data Type=no-repeat
|Description=Image is not repeated.
}}{{CSS Property Value
|Data Type=repeat-x
|Description=Image is repeated horizontally.
}}{{CSS Property Value
|Data Type=repeat-y
|Description=Image is repeated vertically.
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
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''repeat-x''' and '''repeat-y''' values make the image repeat horizontally and vertically, respectively, creating a single band of images from one side to the other.
This property can be set with other background properties by using the [[css/cssom/properties/background|'''background''']] composite property.
In Windows Internet Explorer 9, the background of a box can have multiple layers. The number of layers is determined by the number of comma-separated values in the [[css/properties/background-image|'''background-image''']] property. Each of the images is sized, positioned, and tiled according to the corresponding value in the other background properties ([[css/properties/background-attachment|'''background-attachment''']], [[css/properties/background-clip|'''background-clip''']], [[css/properties/background-origin|'''background-origin''']], [[css/properties/background-position|'''background-position''']], '''background-repeat''', and [[css/properties/background-size|'''background-size''']]). The first image in the list is the layer closest to the user, the next one is painted behind the first, and so on.
|Import_Notes====Syntax===
<code>'''background-repeat: '''repeat '''{{!}}''' repeat-x '''{{!}}''' repeat-y '''{{!}}''' no-repeat</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.3.4
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
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
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}