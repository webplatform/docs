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
|Values={{CSS_Property_Value|Data Type=none |Description=Default. Indicates there is no shadow.}}
{{CSS_Property_Value|Data Type=shadow |Description=A comma-separated list of shadows, each specified by two to four nonzero length values, an optional color, and an optional <code>inset</code> keyword. See Remarks for specific information about usage.}}
}}
{{Topics|CSS}}
{{Notes_Section
|Notes=
===Remarks===
The '''box-shadow''' property can specify one or more drop shadows. The components of each shadow are interpreted as follows:
*Required: The first length is the ''horizontal offset'' of the shadow. A positive value draws a shadow that is offset to the right of the box, a negative length to the left.
*Required: The second length is the ''vertical offset''. A positive value offsets the shadow down, a negative one up.
*Optional: The third length is a ''blur distance''. Negative values are not allowed. If the blur value is zero, the shadow's edge is sharp. Otherwise, the larger the value, the more the shadow's edge is blurred.
*Optional: The fourth length is a ''spread distance''. Positive values cause the shadow shape to expand in all directions by the specified radius. Negative values cause the shadow shape to contract.
*Optional: The ''color'' is the color of the shadow.
*Optional: An <code>inset</code> keyword, if present, changes the drop shadow from an outer shadow (one that shadows the box onto the canvas, as if it were lifted above the canvas) to an inner shadow (one that shadows the canvas onto the box, as if the box were cut out of the canvas and shifted behind it).

|Import_Notes=
===Syntax===
<code>'''box-shadow: '''none '''{{!}}''' ''
&lt;shadow&gt;
''</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}197157 CSS Backgrounds and Borders Module Level 3], Section 6.2


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
|Topic_clusters=Visual Effects
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}