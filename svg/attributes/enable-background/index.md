{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Topics|SVG}}
{{Notes_Section
|Notes=

===Remarks===

The optional ''x'', ''y'', ''width'', ''height''
parameters on the new value are numeric values that indicate the
subregion of the container element's user space where access to the
background image is allowed to happen.  These parameters enable the
SVG user agent potentially to allocate smaller temporary image buffers
than the default values.

|Import_Notes=

===Syntax===

 '''enable-background: '''accumulate '''{{!}}''' new '''[''' ''x'' ''y'' ''width'' ''height'' ''']''''''?''' '''{{!}}''' inherit

===Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}226062 Scalable Vector Graphics: Filter Effects], Section 15.6

}}
{{See_Also_Section
|Manual_sections=

===Related pages (MSDN)===

*[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|'''CSSStyleDeclaration''']]
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}