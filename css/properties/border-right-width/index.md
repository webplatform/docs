{{Page_Title}}
{{Flags
|Content=Not Neutral, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Sets the width of an element's right border.}}
{{CSS Property
|Initial value=medium
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=absolute length; 0 if the border style is 'none' or 'hidden' 
|Animatable=No
|CSS object model property=borderRightWidth
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=medium
|Description=Default.  
}}{{CSS Property Value
|Data Type=thin
|Description=Less than the default width.
}}{{CSS Property Value
|Data Type=thick
|Description=Greater than the default width.
}}{{CSS Property Value
|Data Type=<width>
|Description=Floating-point number, followed by an absolute units designator (<code>cm</code>, <code>mm</code>, <code>in</code>, <code>pt</code>, or <code>pc</code>) or a relative units designator (<code>em</code>, <code>ex</code>, or <code>px</code>). For more information about the supported length units, see CSS Values and Units Reference.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following examples use the '''border-right-width''' attribute and the '''border-right-width''' property to specify the width of the right border.

This example uses a call to an embedded (global) style sheet to change the width of the right border to 1 centimeter when a mouse click occurs.
|Code=&lt;HEAD&gt;
&lt;STYLE&gt;
     TD { border-right-width:3mm }
    .changeborder1 { border-right-width:1cm }
&lt;/STYLE&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;TABLE BORDER&gt;
&lt;TR&gt;
    &lt;TD onclick{{=}}"this.className{{=}}'changeborder1'"
        ondblclick{{=}}"this.className{{=}}''"&gt;
        &lt;IMG src{{=}}"sphere.jpg"&gt;
    &lt;/TD&gt;
&lt;/TR&gt;&lt;/TABLE&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/border-right-width.htm
}}{{Single Example
|Description=This example uses inline script to change the width of the right border to 1 centimeter when a mouse click occurs.
|Code=&lt;TD onclick{{=}}"this.style.borderRightWidth{{=}}'1cm'"&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/borderRightWidth.htm
}}
}}
{{Notes_Section
|Notes=
As of Microsoft Internet Explorer 5.5, this property applies to inline elements.  With earlier versions of  Windows Internet Explorer, inline elements must have an '''absolute''' [[css/properties/position|'''position''']] or layout to use this property. Element layout is set by providing a value for the [[css/properties/height|'''height''']] property or the [[css/properties/width|'''width''']] property.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Backgrounds and Borders Module Level 3
|URL=http://www.w3.org/TR/css3-background/#the-border-width
|Status=Candidate Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Border
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Reference</code>
*<code>[[css/properties/border|border]]</code>
*<code>[[css/properties/border-width|border-width]]</code>
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