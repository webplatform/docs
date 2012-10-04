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
{{Examples_Section
|Not_required=No
|Examples=}}
{{Notes_Section
|Notes=
===Remarks===
Spellcheck is only enabled by default  '''textArea''' elements, and elements with the [[html/attributes/contentEditable|'''contentEditable''']] {{=}} true attribute for  Metro style apps using JavaScript, Internet Explorer 10, and Internet Explorer 10 for the desktop in Windows 8. Spellcheck is off by default for '''input type{{=}}text'''
Spellcheck is off by default of any element in the apps that host the web browser control (Web OC). You  can enable spellchecking by adding the '''spellcheck{{=}}true''' attribute to the root or ancestor markup of the content (including the &lt;html&gt; element), with no other special flags needed.
There is also a default state (missing attribute) which uses the element's default behavior, such as inheriting from the parent element's spellcheck state.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/HTMLElement|HTMLElement]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}