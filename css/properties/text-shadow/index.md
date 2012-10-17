{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS Property
|Initial value=none
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=none
|Description=Default. Indicates there is no shadow.
}}{{CSS Property Value
|Data Type=shadow
|Description=A comma-separated list of shadows, each specified by two to four nonzero length values and an optional color. See Remarks for specific information about usage.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The following example applies a dark gray shadow with a small blur value slightly to the right and under the specified text:
|Code=.myselector 
{
...
  text-shadow: 0.1em 0.1em 0.15em #333;
}
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''text-shadow''' property can specify one or more drop shadows. The components of each shadow are interpreted as follows:
*Required: The first length is the ''horizontal offset'' of the shadow. A positive value draws a shadow that is offset to the right of the box, a negative length to the left.
*Required: The second length is the ''vertical offset''. A positive value offsets the shadow down, a negative one up.
*Optional: The third length is a ''blur distance''. Negative values are not allowed. If the blur value is zero, the shadow's edge is sharp. Otherwise, the larger the value, the more the shadow's edge is blurred.
*Optional: The fourth length is a ''spread distance''. Positive values cause the shadow shape to expand in all directions by the specified radius. Negative values cause the shadow shape to contract.
*Optional: The ''color'' is the color of the shadow.
|Import_Notes====Syntax===
<code>'''text-shadow: '''none '''{{!}}''' ''
&lt;shadow&gt;
''</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203766 CSS Text Level 3], Section 11.3
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
|Topic_clusters=Text
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}