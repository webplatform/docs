{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_Property
|Applies to=All elements
|Media=visual
|Inherited=Yes
|Initial value=none
|Values={{CSS_Property_Value|Data Type=none |Description=Default. Indicates there is no shadow.}}
{{CSS_Property_Value|Data Type=shadow |Description=A comma-separated list of shadows, each specified by two to four nonzero length values and an optional color. See Remarks for specific information about usage.}}
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example applies a dark gray shadow with a small blur value slightly to the right and under the specified text:
|LiveURL=
|Code=
.myselector 
{
...
  text-shadow: 0.1em 0.1em 0.15em #333;
}
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''text-shadow''' property can specify one or more drop shadows. The components of each shadow are interpreted as follows:
*Required: The first length is the ''horizontal offset'' of the shadow. A positive value draws a shadow that is offset to the right of the box, a negative length to the left.
*Required: The second length is the ''vertical offset''. A positive value offsets the shadow down, a negative one up.
*Optional: The third length is a ''blur distance''. Negative values are not allowed. If the blur value is zero, the shadow's edge is sharp. Otherwise, the larger the value, the more the shadow's edge is blurred.
*Optional: The fourth length is a ''spread distance''. Positive values cause the shadow shape to expand in all directions by the specified radius. Negative values cause the shadow shape to contract.
*Optional: The ''color'' is the color of the shadow.

|Import_Notes=
===Syntax===
<code>'''text-shadow: '''none '''{{!}}''' ''
&lt;shadow&gt;
''</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203766 CSS Text Level 3], Section 11.3


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
|Topic_clusters=Text
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}