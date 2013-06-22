{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=Yes
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS Property
|Initial value=not defined for shorthand properties
|Applies to=inline-level and ‘table-cell’ elements
|Inherited=No
|Media=visual
|Animatable=No
|CSS percentages=refers to the ‘line-height’ of the element itself
|Values={{CSS Property Value
|Data Type=auto
|Description=Aligns the contents of an object according to the value of the [[css/properties/layout-flow|'''-ms-layout-flow''']] attribute.
}}{{CSS Property Value
|Data Type=baseline
|Description=Default. Aligns the contents of an object supporting [[html/attributes/vAlign|'''VALIGN''']] to the base line.
}}{{CSS Property Value
|Data Type=sub
|Description=Vertically aligns the text to subscript.
}}{{CSS Property Value
|Data Type=super
|Description=Vertically aligns the text to superscript.
}}{{CSS Property Value
|Data Type=top
|Description=Vertically aligns the contents of an object supporting [[html/attributes/vAlign|'''VALIGN''']] to the top of the object.
}}{{CSS Property Value
|Data Type=middle
|Description=Vertically aligns the contents of an object supporting [[html/attributes/vAlign|'''VALIGN''']] to the middle of the object.
}}{{CSS Property Value
|Data Type=bottom
|Description=Vertically aligns the contents of an object supporting [[html/attributes/vAlign|'''VALIGN''']] to the bottom of the object.
}}{{CSS Property Value
|Data Type=text-top
|Description=Vertically aligns the text of an object supporting [[html/attributes/vAlign|'''VALIGN''']] to the top of the object.
}}{{CSS Property Value
|Data Type=text-bottom
|Description=Vertically aligns the text of an object supporting [[html/attributes/vAlign|'''VALIGN''']] to the bottom of the object.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the '''vertical-align''' property to align text within a table cell.
|Code=&lt;TABLE BORDER width{{=}}100&gt;
&lt;TR&gt;
    &lt;TD onmouseover{{=}}"this.style.verticalAlign{{=}}'bottom'" 
    onmouseout{{=}}"this.style.verticalAlign{{=}}''"&gt;
    text to align&lt;/TD&gt; 
&lt;/TR&gt;
&lt;/TABLE&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/verticalAlign.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''sub''' and <code>super</code> values are supported on text. The '''auto''' value is supported on the [[css/cssom/currentStyle|'''currentStyle''']] object.  The other values are supported on objects that support [[html/attributes/vAlign|'''VALIGN''']].
The '''auto''' value is identical to the '''baseline''' value when the [[css/properties/layout-flow|'''-ms-layout-flow''']] is '''horizontal'''.  When the '''-ms-layout-flow''' is '''vertical-ideographic''', the '''auto''' value is identical to the '''middle''' value.
|Import_Notes====Syntax===
<code>'''vertical-align: '''baseline '''{{!}}''' sub '''{{!}}''' super '''{{!}}''' top '''{{!}}''' text-top '''{{!}}''' middle '''{{!}}''' bottom '''{{!}}''' text-bottom</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.4.4
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=4.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=4.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
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
*<code>[[html/attributes/vAlign|vAlign]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}