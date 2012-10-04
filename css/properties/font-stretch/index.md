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
|Initial value=
|Values={{CSS_Property_Value|Data Type=normal |Description=Default. Indicates the face is neither condensed nor expanded.}}
{{CSS_Property_Value|Data Type=wider |Description=Indicates a wider value relative to the width of the parent element.}}
{{CSS_Property_Value|Data Type=narrower |Description=Indicates a narrower value relative to the width of the parent element.}}
{{CSS_Property_Value|Data Type=ultra-condensed |Description=Indicates the most condensed font face.}}
{{CSS_Property_Value|Data Type=extra-condensed |Description=Indicates the second most condensed font face.}}
{{CSS_Property_Value|Data Type=condensed |Description=Indicates a condensed font face.}}
{{CSS_Property_Value|Data Type=semi-condensed |Description=Indicates a slightly condensed font face.}}
{{CSS_Property_Value|Data Type=semi-expanded |Description=Indicates a slightly expanded font face.}}
{{CSS_Property_Value|Data Type=expanded |Description=Indicates an expanded font face.}}
{{CSS_Property_Value|Data Type=extra-expanded |Description=Indicates the second most expanded font face.}}
{{CSS_Property_Value|Data Type=ultra-expanded |Description=Indicates the most expanded font face.}}
{{CSS_Property_Value|Data Type=inherit |Description=Indicates that the property takes the same computed value as the property for the element's parent.}}
}}
{{Topics|CSS}}
{{Notes_Section
|Notes=
===Remarks===
Absolute keyword values have the following order, from narrowest to widest:
*Ultra condensed
*Extra condensed
*Condensed
*Semi condensed
*Normal
*Semi expanded
*Expanded
*Extra expanded
*Ultra expanded

The scale is relative, so a font face that has a font-stretch value  higher in the previous list above should never appear wider. When a font face does not exist for a given width, normal or condensed values map to a narrower font face. Otherwise, they map to a wider font face. Conversely, expanded values map to a wider font face; otherwise, a narrower face.
|Import_Notes=
===Syntax===
<code>'''font-stretch: '''normal '''{{!}}''' wider '''{{!}}''' narrower '''{{!}}''' ultra-condensed '''{{!}}''' extra-condensed '''{{!}}''' condensed '''{{!}}''' semi-condensed '''{{!}}''' semi-expanded '''{{!}}''' expanded '''{{!}}''' extra-expanded '''{{!}}''' ultra-expanded '''{{!}}''' inherit</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199818 Scalable Vector Graphics: Text], Section 10.10


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>LayoutRect</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>style</code>
*<code>[[css/properties/font-size-adjust|font-size-adjust]]</code>
|Topic_clusters=Fonts
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}