{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/HTMLElement
|Read_only=
}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
The value of the '''offscreenBuffering''' property determines how the current document is drawn. When the property is set to '''true''', objects are added to an offscreen buffer. After all objects are drawn, the contents of the offscreen buffer are made visible to the user. When the property is set to '''false''', objects are rendered directly to the screen.
By default, Internet Explorer decides when to buffer objects offscreen. In addition, Internet Explorer automatically enables offscreen buffering when Microsoft DirectX-based components are used on the document.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>window</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}