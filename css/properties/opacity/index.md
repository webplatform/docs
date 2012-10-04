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
|Initial value=1
|Values={{CSS_Property_Value|Data Type=&lt;alphavalue&gt; |Description=A '''Floating-point''' value between 0.0 (fully transparent) and 1.0 (fully opaque), inclusive.}}
{{CSS_Property_Value|Data Type=inherit |Description=Indicates that the property takes the same computed value as the property for the element's parent.}}
}}
{{Topics|CSS}}
{{Notes_Section
|Notes=
===Remarks===
The opacity setting is applied uniformly across the entire object. Any values outside the range 0.0 to 1.0 will be clamped to this range.
Object or group opacity can be thought of conceptually as a postprocessing operation. Conceptually, after the object or group is rendered into an RGBA offscreen image, the object or group opacity setting specifies how to blend the offscreen image into the current background.
|Import_Notes=
===Syntax===
<code>'''opacity: '''&lt;alphavalue&gt; '''{{!}}''' inherit</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203761 CSS Color Module Level 3], Section 3.2


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[svg/properties/a|a]]</code>
|Topic_clusters=Visual Effects
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}