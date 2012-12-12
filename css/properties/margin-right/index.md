{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Sets the right margin of an element.}}
{{CSS Property
|Initial value=0
|Applies to=All elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=margin-width
|Description=Default. Right margin is set equal to the left margin.
}}{{CSS Property Value
|Data Type=inherit
|Description=Integer, followed by a percent sign (%). The value is a percentage of the width of the parent object.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following examples use the '''margin-right''' attribute and the '''marginRight''' property to change the margin of the object.

This example uses '''img''' as a selector and <code>margin1</code> as a class in an embedded style sheet to set the right margin of an image when an [[dom/events/click|'''onclick''']] event or [[dom/events/dblclick|'''ondblclick''']] event occurs.
|Code=&lt;STYLE&gt;
    IMG { margin-right:1cm }
    .margin1 { margin-right:2cm }
&lt;/STYLE&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;IMG src{{=}}"sphere.jpg" onclick{{=}}"this.className{{=}}'margin1'"
    ondblclick{{=}}"this.className{{=}}''"&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/margin-right.htm
}}{{Single Example
|Description=This example uses inline scripting to set the right margin of the image to 1 centimeter when the [[dom/events/click|'''onclick''']] event occurs.
|Code=&lt;IMG src{{=}}"sphere.jpeg" onclick{{=}}"this.style.marginRight{{=}}'1cm'"&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/marginRight.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
You can specify possible length values relative to the height of the element's font (<code>em</code>) or the height of the letter "x" (<code>ex</code>).
In Microsoft Internet Explorer 3.0, the specified margin value is added to the default value of the object. In Microsoft Internet Explorer 4.0 and later, the margin value is absolute. The margin properties do not work with the '''td''' and '''tr''' objects in Internet Explorer 4.0, but they do work in Internet Explorer 3.0. To set margins in the cell for Internet Explorer 4.0 and later, apply the margin to an object, such as '''div''' or '''p''', within the '''td'''.
This property applies to inline elements,   starting with Microsoft Internet Explorer 5.5.  With earlier versions of  Windows Internet Explorer, inline elements must have an '''absolute''' [[css/properties/position|'''position''']] or layout to use this property. Element layout is set by providing a value for the [[css/properties/height|'''height''']] property or the [[css/properties/width|'''width''']] property.
Negative margins are supported, except for top and bottom margins on inline objects.
|Import_Notes====Syntax===
<code>'''margin-right: '''''
&lt;margin-width&gt;
'' '''{{!}}''' inherit</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.5.2
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Box Model
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Conceptual</code>
*<code>CSS Values and Units Reference</code>
*<code>Other Resources</code>
*<code>CSS Enhancements in Internet Explorer 6</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}