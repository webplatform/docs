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
|Values={{CSS_Property_Value|Data Type=
CSSStyleDeclaration
|Description=[[css/cssom/currentStyle|'''currentStyle''']]}}
{{CSS_Property_Value|Data Type=
currentStyle
|Description=[[dom/defaultSelected|'''defaults''']]}}
{{CSS_Property_Value|Data Type=
defaults
|Description=[[css/cssom/runtimeStyle|'''runtimeStyle''']]}}
{{CSS_Property_Value|Data Type=
runtimeStyle
|Description=[[css/cssom/style|'''style''']]}}
{{CSS_Property_Value|Data Type=
style
|Description=[[css/properties/border|'''border''']]}}
{{CSS_Property_Value|Data Type=
border
|Description=}}
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following examples use the '''border-left-style''' attribute and the '''border-left-style''' property to specify the style of the left border.

This example uses a call to an embedded (global) style sheet to change the style of the left border from '''solid''' to '''groove''' when an [[dom/events/mouseover|'''onmouseover''']] event occurs.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/border-left-style.htm
|Code=
&lt;HEAD&gt;
&lt;STYLE&gt;
    TD { border-left-style:solid; border-width:0.3cm }
    .change { border-left-style:groove }
&lt;/STYLE&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;TABLE BORDER&gt;
&lt;TR&gt;
    &lt;TD onmouseover{{=}}"this.className{{=}}'change'"
        onmouseout{{=}}"this.className{{=}}''"&gt;
        &lt;IMG src{{=}}"sphere.jpg"&gt;
    &lt;/TD&gt;
&lt;/TR&gt; 
&lt;/TABLE&gt;
}}
{{Single_Example
|Description=This example uses inline scripting to change the style of the left border to '''groove''' when an [[dom/events/mouseover|'''onmouseover''']] event occurs.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/borderLeftStyle.htm
|Code=
&lt;TD onmouseover{{=}}"this.style.borderWidth{{=}}'0.5cm';
                 this.style.borderLeftStyle{{=}}'groove'"&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
A [[css/properties/border-width|'''border-width''']] greater than 0 must be set for the '''border-left-style''' attribute to render.
As of Internet Explorer 5.5, this property applies to inline elements.  With earlier versions of  Internet Explorer, inline elements must have an '''absolute''' [[css/properties/position|'''position''']] or layout to use this property. Element layout is set by providing a value for the [[css/properties/height|'''height''']] property or the [[css/properties/width|'''width''']] property.
|Import_Notes=
===Syntax===
<code>'''border-left-style: '''none '''{{!}}''' dotted '''{{!}}''' dashed '''{{!}}''' solid '''{{!}}''' double '''{{!}}''' groove '''{{!}}''' ridge '''{{!}}''' inset '''{{!}}''' outset '''{{!}}''' window-inset '''{{!}}''' hidden</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 8.5.3


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[css/properties/border|border]]</code>
|Topic_clusters=Border
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}