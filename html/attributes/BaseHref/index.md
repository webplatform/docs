{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Topics|HTML}}
{{Notes_Section
|Notes=
===Remarks===
Use the '''BaseHref''' property to resolve relative paths when locating an '''object'''.  The following rules determine the resulting ''p''.
*If the '''object''' element is on a page containing a '''base''' element, then ''p'' takes the value of the '''base'''.[[html/attributes/href (base)|'''href''']] property.
*If the '''object''' element is on a page with <code>javascript</code> or  <code>vbscript</code>, or is about '''protocol''' URLs, then ''p'' takes the value of the current page's parent page URL.  This applies to '''object'''.'''BaseHref''' property requests in '''iframe'''/ '''frame''' elements as well.
*For all other '''object''' elements, ''p'' takes the value of the page they are found on.

|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>object</code>
|Topic_clusters=html
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}