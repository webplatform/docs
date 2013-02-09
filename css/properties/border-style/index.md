{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Sets the style of an element's four borders. This property can have from one to four values.}}
{{CSS Property
|Initial value=none
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=specified value
|Animatable=No
|CSS object model property=borderStyle
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=none
|Description=Default. Border is not drawn, regardless of any [[css/properties/border-width|'''border-width''']].
}}{{CSS Property Value
|Data Type=hidden
|Description=Internet Explorer 8. Same as <code>none</code>, except in terms of conflict resolution of collapsed borders. Any element with a <code>hidden</code> border suppresses all shared borders at that location. Borders with a style of none have the lowest priority.
}}{{CSS Property Value
|Data Type=dotted
|Description=Border is a dotted line.
}}{{CSS Property Value
|Data Type=dashed
|Description=Border is a dashed line.
}}{{CSS Property Value
|Data Type=solid
|Description=Border is a solid line.
}}{{CSS Property Value
|Data Type=double
|Description=Border is a double line drawn on top of the background of the object. The sum of the two single lines and the space between equals the [[css/properties/border-width|'''border-width''']] value. The border width must be at least 3 pixels wide to draw a double border.
}}{{CSS Property Value
|Data Type=groove
|Description=3-D groove is drawn in colors based on the value.
}}{{CSS Property Value
|Data Type=ridge
|Description=3-D ridge is drawn in colors based on the value.
}}{{CSS Property Value
|Data Type=inset
|Description=3-D inset is drawn in colors based on the value.
}}{{CSS Property Value
|Data Type=outset
|Description=3-D outset is drawn in colors based on the value.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following examples use the '''border-style''' attribute and the '''border-style''' property to specify the border style.

This example uses a call to an embedded (global) style sheet to change the style of the border to '''groove''' when an [[dom/events/mouseover|'''onmouseover''']] event occurs.
|Code=&lt;head&gt;
&lt;style type{{=}}"text/css"&gt;
td {
    border-style: solid;
    border-width: 0.5cm;
}
.change {
    border-style: groove;
}
&lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;table border{{=}}""&gt;
    &lt;tr&gt;
        &lt;td onmouseover{{=}}"this.className{{=}}'change'" onmouseout{{=}}"this.className{{=}}''"&gt;
            &lt;img src{{=}}"sphere.jpg" alt{{=}}"sphere image"&gt; 
        &lt;/td&gt;
    &lt;/tr&gt;
&lt;/table&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/border-style.htm
}}{{Single Example
|Description=This example uses inline scripting to change the style of the border to '''groove''' when an [[dom/events/mouseover|'''onmouseover''']] event occurs.
|Code=&lt;td onmouseover{{=}}"this.style.borderWidth{{=}}'0.5cm';
    this.style.borderStyle{{=}}'groove'"&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/borderStyle.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
As of Internet Explorer 5.5, this property applies to inline elements.  With earlier versions of  Internet Explorer, inline elements must have an '''absolute''' [[css/properties/position|'''position''']] or layout to use this property. Element layout is set by providing a value for the [[css/properties/height|'''height''']] property or the [[css/properties/width|'''width''']] property.
|Import_Notes====Syntax===
<code>'''border-style: '''none '''{{!}}''' dotted '''{{!}}''' dashed '''{{!}}''' solid '''{{!}}''' double '''{{!}}''' groove '''{{!}}''' ridge '''{{!}}''' inset '''{{!}}''' outset '''{{!}}''' window-inset '''{{!}}''' hidden</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.5.17
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
|Topic_clusters=Border
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[css/properties/border|border]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}