{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/document
|Read_only=
}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
You cannot execute script when the value of the '''designMode''' property is set to '''On'''.
You can use the '''designMode''' property to put Windows Internet Explorer into a mode so that you can edit the current document.
While the browser is in design mode, objects enter a UI-activated state when the user presses <code>ENTER</code>, clicks an object that has focus, or double-clicks the object. Objects that are UI-activated have their own window in the document. You can modify the UI only when the object is in a UI-activated state.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/document|document]]</code>
*<code>Introduction to MSHTML Editing</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}