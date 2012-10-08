{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS Property
|Applies to=All elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=scroll
|Description=Default. Background image scrolls with the object as the document is scrolled.
}}{{CSS Property Value
|Data Type=fixed
|Description=Background image stays fixed within the viewable area of the object.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following examples use the '''background-attachment''' attribute and the '''background-attachment''' property to set the background to "fixed", so that the background does not scroll with the text.

This example uses an inline style sheet to set the background to fixed.
|Code=&lt;STYLE &gt;
    BODY { background-attachment:fixed }
&lt;/STYLE&gt;
&lt;/HEAD&gt;
&lt;BODY background{{=}}"some.jpg"&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/background-attachment.htm
}}{{Single Example
|Description=This example uses inline scripting to set the background to fixed.
|Code=&lt;BODY ID{{=}}"oBdy" background{{=}}"marble05.jpg"
onload{{=}}"oBdy.style.backgroundAttachment {{=}} 'fixed'"&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/backgroundAttachment.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
This property can be set with the other background properties by using the [[css/cssom/properties/background|'''background''']] composite property.
Microsoft Internet Explorer 3.0 supports the '''background-attachment''' attribute, but only when it's set by using the [[css/cssom/properties/background|'''background''']] attribute.
In Windows Internet Explorer 9, the background of a box can have multiple layers. The number of layers is determined by the number of comma-separated values in the [[css/properties/background-image|'''background-image''']] property. Each of the images is sized, positioned, and tiled according to the corresponding value in the other background properties ('''background-attachment''', [[css/properties/background-clip|'''background-clip''']], [[css/properties/background-origin|'''background-origin''']], [[css/properties/background-position|'''background-position''']], [[css/properties/background-repeat|'''background-repeat''']], and [[css/properties/background-size|'''background-size''']]). The first image in the list is the layer closest to the user, the next one is painted behind the first, and so on.
|Import_Notes====Syntax===
<code>'''background-attachment: '''scroll '''{{!}}''' fixed</code>
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
*<code>LayoutRect</code>
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