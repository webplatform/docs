{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS Property
|Applies to=All elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=normal
|Description=Default. Element does not open an additional level of embedding. For inline elements, implicit reordering works across element boundaries.
}}{{CSS Property Value
|Data Type=embed
|Description=Element opens an additional level of embedding. The value of the [[css/properties/direction|'''direction''']] property specifies the embedding level. Reordering is implicit inside the element.
}}{{CSS Property Value
|Data Type=bidi-override
|Description=Same as the <code>embed</code> value, except that, inside the element, reordering is strictly in sequence according to the [[css/properties/direction|'''direction''']] property. This value overrides the implicit bidirectional algorithm.
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
The '''unicode-bidi''' property is used with the [[css/properties/direction|'''direction''']] property.
The Unicode bidirectional algorithm automatically reverses embedded character sequences according to their inherent direction. For example, the base direction of an English document is left-to-right. If portions of a paragraph within the document contain a language with a right-to-left reading order, the direction of that language displays correctly right-to-left. The user agent applying the bidirectional algorithm correctly reverses the language direction.
|Import_Notes====Syntax===
<code>'''unicode-bidi: '''normal '''{{!}}''' embed '''{{!}}''' bidi-override</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 9.10
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=2.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Yes
|Internet_explorer_prefixed_version=5.5
|Opera_supported=Yes
|Opera_version=9.2
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.3
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}