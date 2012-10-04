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
|Initial value=0
|Values={{CSS_Property_Value|Data Type=margin-width |Description=Default. Left margin is set equal to the right margin.}}
{{CSS_Property_Value|Data Type=inherit |Description=Integer, followed by a percent sign (%). The value is a percentage of the width of the parent object.}}
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following examples use the '''margin-left''' attribute and the '''marginLeft''' property to change the margin of the object.

This example uses the '''img''' object as a selector to set the left margin to 2 centimeters for all images.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/margin-left.htm
|Code=
&lt;STYLE&gt;
    IMG { margin-left:2cm }
&lt;/STYLE&gt;
}}
{{Single_Example
|Description=This example uses inline scripting to set the left margin of the image to 1 centimeter when an [[dom/events/click|'''onclick''']] event occurs.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/marginLeft.htm
|Code=
&lt;IMG src{{=}}"sphere.jpg" onclick{{=}}"this.style.marginLeft{{=}}'1cm'"&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
You can specify possible length values relative to the height of the element's font (<code>em</code>) or the height of the letter "x" (<code>ex</code>).
In Microsoft Internet Explorer 3.0, the specified margin value is added to the default value of the object. In Microsoft Internet Explorer 4.0 and later, the margin value is absolute. The margin properties do not work with the '''td''' and '''tr''' objects in Internet Explorer 4.0, but they do work in Internet Explorer 3.0. To set margins in the cell for Internet Explorer 4.0 and later, apply the margin to an object, such as '''div''' or '''p''', within the '''td'''.
This property applies to inline elements, starting with Microsoft Internet Explorer 5.5.  With earlier versions of  Windows Internet Explorer, inline elements must have an '''absolute''' [[css/properties/position|'''position''']] or layout to use this property. Element layout is set by providing a value for the [[css/properties/height|'''height''']] property or the [[css/properties/width|'''width''']] property.
Negative margins are supported, except for top and bottom margins on inline objects.
|Import_Notes=
===Syntax===
<code>'''margin-left: '''''
&lt;margin-width&gt;
'' '''{{!}}''' inherit</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.5.4


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Conceptual</code>
*<code>CSS Values and Units Reference</code>
*<code>Other Resources</code>
*<code>CSS Enhancements in Internet Explorer 6</code>
|Topic_clusters=Box Model
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}