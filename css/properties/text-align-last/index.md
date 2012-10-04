{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_Property
|Applies to=block containers
|Media=visual
|Inherited=Yes
|Initial value=auto
|Values={{CSS_Property_Value|Data Type=auto |Description=Default. Text is aligned like the other lines in the object, using the value of the [[css/properties/text-align|'''text-align''']] property.}}
{{CSS_Property_Value|Data Type=center |Description=Text is centered.}}
{{CSS_Property_Value|Data Type=inherit |Description=Text is aligned like the text in the parent object.}}
{{CSS_Property_Value|Data Type=justify |Description=Text is justified.}}
{{CSS_Property_Value|Data Type=left |Description=Text is aligned to the left.}}
{{CSS_Property_Value|Data Type=right |Description=Text is aligned to the right.}}
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example shows an embedded style rule that justifies all the lines in the document's '''p''' elements.  This is commonly found in East Asian typography.
|LiveURL=
|Code=
&lt;style&gt;
    p.DistributeAllLines { text-align: justify;
                           text-justify: distribute;                             
                           text-align-last: justify }
&lt;/style&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
Windows Internet Explorer 8. The '''-ms-text-align-last''' property is an extension to Cascading Style Sheets (CSS), and can be used as a synonym for the '''text-align-last''' property in IE8 Standards mode and higher.
|Import_Notes=
===Syntax===
<code>'''-ms-text-align-last: '''auto '''{{!}}''' center '''{{!}}''' inherit '''{{!}}''' justify '''{{!}}''' left '''{{!}}''' right</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203766 CSS Text Level 3], Section 8.1


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
|Topic_clusters=Text
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}