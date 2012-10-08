{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS Property
|Initial value=0
|Applies to=All elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=margin-width
|Description=Default. Top margin is set equal to the bottom margin.
}}{{CSS Property Value
|Data Type=inherit
|Description=Integer, followed by a percent sign (%). The value is a percentage of the height of the parent object.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following examples use the '''margin-top''' attribute and the '''margin-top''' property to change the margin of the object.

This example uses '''hr''' as a selector and <code>margin1</code> as a class in an embedded style sheet to set the top margin of the horizontal rule.
|Code=&lt;STYLE&gt;
    HR { margin-top:2cm }
    .margin1 { margin-top:4cm }
&lt;/STYLE&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;HR onclick{{=}}"this.className{{=}}'margin1'" ondblclick{{=}}"this.className{{=}}''"&gt;
&lt;/STYLE&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/margin-top.htm
}}{{Single Example
|Description=This example uses inline scripting to set and reset the margin when the [[dom/events/click|'''onclick''']] and [[dom/events/dblclick|'''ondblclick''']] events occur, respectively.
|Code=&lt;HR onclick{{=}}"this.style.marginTop{{=}}'2cm'" 
ondblclick{{=}}"this.style.marginTop{{=}}''"&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/marginTop.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
As of Microsoft Internet Explorer 4.0 or later, you can specify possible length values relative to the height of the element's font (<code>em</code>) or the height of the letter "x" (<code>ex</code>).
In Microsoft Internet Explorer 3.0, the specified margin value is added to the default value of the object. In Internet Explorer 4.0 or later, the margin value is absolute. The margin properties do not work with the '''td''' and '''tr''' objects in Internet Explorer 4.0, but they do work in Internet Explorer 3.0. To set margins in the cell for Internet Explorer 4.0 or later, apply the margin to an object, such as '''div''' or '''p''', within the '''td'''.
As of Microsoft Internet Explorer 5.5, this property applies to inline elements. With earlier versions of Windows Internet Explorer, inline elements must have an '''absolute''' [[css/properties/position|'''position''']] or layout to use this property. Element layout is set by providing a value for the [[css/properties/height|'''height''']] property or the [[css/properties/width|'''width''']] property.
For inline elements, the value of this property is used to compute the border area of a surrounding inline element, if present.  This value does not contribute to the height of a line.
Negative margins are supported, except for top and bottom margins on inline objects.
|Import_Notes====Syntax===
<code>'''margin-top: '''''
&lt;margin-width&gt;
'' '''{{!}}''' inherit</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.5.1
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