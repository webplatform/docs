{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The padding property defines the space between the content box within an element  and its border.}}
{{CSS Property
|Applies to=All elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=length
|Description=Floating-point number, followed by an absolute units designator (<code>cm</code>, <code>mm</code>, <code>in</code>, <code>pt</code>, or <code>pc</code>) or a relative units designator (<code>em</code>, <code>ex</code>, or <code>px</code>). For more information about the supported length units, see CSS Values and Units Reference.
}}{{CSS Property Value
|Data Type=percentage
|Description=Integer, followed by a %. The value is a percentage of the width of the parent object.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following examples use the '''padding''' attribute and the '''padding''' property to change the padding of the object.

This example uses '''td''' as a selector and <code>padding1</code> as a class in an embedded style sheet to set the padding for the '''td''' object.
|Code=&lt;STYLE&gt;
    TD { padding:3mm 8mm }
    .padding1  { padding:1cm }
&lt;/STYLE&gt;
&lt;/HEAD&gt; 
&lt;BODY&gt; 
&lt;TABLE BORDER&gt;
    &lt;TD onmouseover{{=}}"this.className{{=}}'padding1'"
    onmouseout{{=}}"this.className{{=}}''" ALIGN{{=}}middle&gt;
    &lt;IMG src{{=}}"sphere.jpg"&gt;
    &lt;/TD&gt;
&lt;/TABLE&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/padding_h.htm
}}{{Single Example
|Description=This example uses inline scripting to set the cell's top and bottom padding to 0.5 centimeters and its left and right padding to 0.2 centimeters when an [[dom/events/mouseover|'''onmouseover''']] event occurs.
|Code=&lt;TD onmouseover{{=}}"this.style.padding{{=}}'0.5cm 0.2cm'"
    onmouseout{{=}}"this.style.padding{{=}}''" ALIGN{{=}}middle&gt;
    &lt;IMG src{{=}}"sphere.jpeg"&gt;
&lt;/TD&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/padding_s.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
This is a composite property that specifies up to four padding values, in the following order: top, right, bottom, left. If one width value is specified, it is used for all four sides. If two width values are specified, the first is used for the top and bottom borders, and the second is used for left and right borders. If three width values are specified, they are used for top, right/left, and bottom borders, respectively. Negative values are not allowed.
As of Microsoft Internet Explorer 5.5, this property applies to inline elements.  With earlier versions of  Windows Internet Explorer, inline elements must have an '''absolute''' [[css/properties/position|'''position''']] or layout to use this property. Element layout is set by providing a value for the [[css/properties/height|'''height''']] property or the [[css/properties/width|'''width''']] property.
|Import_Notes====Syntax===
<code>'''padding: '''''
&lt;length&gt;
'' '''{{!}}''' ''
&lt;percentage&gt;
''</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.5.10
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