{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{CSS_Property
|Applies to=box elements
|Media=visual
|Inherited=No
|Initial value=normal
|Values={{CSS_Property_Value|Data Type=normal |Description=Default. 
Child elements are displayed in the same order that they are declared in the source document. 

If the parent element has a computed value for [[css/properties/ms-box-orient|'''-ms-box-orient''']] of <code>horizontal</code>, the child elements are displayed from left to right. 

If the parent element has a computed value for [[css/properties/ms-box-orient|'''-ms-box-orient''']] of <code>vertical</code>, the child elements are displayed from top to bottom.}}
{{CSS_Property_Value|Data Type=reverse |Description=Child elements are displayed in the reverse order that they are declared in the source document. 

If the parent element has a computed value for [[css/properties/ms-box-orient|'''-ms-box-orient''']] of <code>horizontal</code>, the child elements are displayed from right to left. 

If the parent element has a computed value for [[css/properties/ms-box-orient|'''-ms-box-orient''']] of <code>vertical</code>, the child elements are displayed from bottom to top.}}
{{CSS_Property_Value|Data Type=inherit |Description=Child elements are displayed in the same order as the computed value of this property for the parent element.}}
}}
{{Topics|CSS}}
{{Notes_Section
|Import_Notes=
===Syntax===
<code>'''-ms-box-direction: '''normal '''{{!}}''' reverse '''{{!}}''' inherit</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}223142 Flexible Box Layout Module], Section 3


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
|Topic_clusters=Flexbox
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}