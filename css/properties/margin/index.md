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
|Values={{CSS_Property_Value|Data Type=top |Description=Any of the range of margin width values available to the [[css/properties/margin-top|'''margin-top''']] property.}}
{{CSS_Property_Value|Data Type=right |Description=Any of the range of margin width values available to the [[css/properties/margin-right|'''margin-right''']] property.}}
{{CSS_Property_Value|Data Type=bottom |Description=Any of the range of margin width values available to the [[css/properties/margin-bottom|'''margin-bottom''']] property.}}
{{CSS_Property_Value|Data Type=left |Description=Any of the range of margin width values available to the [[css/properties/margin-left|'''margin-left''']] property.}}
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following examples use the '''margin''' attribute and the '''margin''' property to change the margin of the object.

This example uses the '''img''' object as a selector to set the margin of images to 1 centimeter.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/margin_h.htm
|Code=
&lt;STYLE&gt;
    IMG { margin:1cm }
&lt;/STYLE&gt;
}}
{{Single_Example
|Description=This example uses inline scripting to set the margin of the image to 5 millimeters when an [[dom/events/mouseover|'''onmouseover''']] event occurs.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/margin_s.htm
|Code=
&lt;IMG src{{=}}"sphere.jpg" onmouseover{{=}}"this.style.margin{{=}}'5mm'"&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
This is a composite property that specifies up to four width values, in the following order: top, right, bottom, left. If one width value is specified, it is used for all four sides. If two width values are specified, the first is used for the top and bottom borders, and the second is used for left and right borders. If three width values are specified, they are used for the top, right/left, and bottom borders, respectively. Negative margins are supported except for top and bottom margins on inline objects.
As of Microsoft Internet Explorer 4.0, you can specify length values relative to the height of the element's font (<code>em</code>) or the height of the letter "x" (<code>ex</code>).
In Microsoft Internet Explorer 3.0, the specified margin value is added to the default value of the object. In Internet Explorer 4.0 or later, the margin value is absolute. The margin properties do not work with the '''td''' and '''tr''' objects in Internet Explorer 4.0, but they do work in Internet Explorer 3.0. To set margins in the cell for Internet Explorer 4.0 or later, apply the margin to an object, such as '''div''' or '''p''', within the '''td'''.
As of Microsoft Internet Explorer 5.5, this property applies to inline elements.  With earlier versions of  Windows Internet Explorer, inline elements must have an '''absolute''' [[css/properties/position|'''position''']] or layout to use this property. Element layout is set by providing a value for the [[css/properties/height|'''height''']] property or the [[css/properties/width|'''width''']] property.
For inline elements, the '''top''' and '''bottom''' values are used to compute the border area of a surrounding inline element, if present. These values do not contribute to the height of a line.
Margins are always transparent.
|Import_Notes=
===Syntax===
<code>'''margin: '''top '''{{!}}''' right '''{{!}}''' bottom '''{{!}}''' left</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.5.5


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