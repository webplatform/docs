{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=bstrText|Data type=BSTR|Description=The text that replaces the existing text.|Optional=}}
|Method_applies_to=dom/TextNode
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description='''IHTMLDOMNode'''

A [[dom/TextNode|'''TextNode''']] object that received the replacement text.  If the replaced text was empty, this value will be null. If the current node is read-only, a new '''TextNode''' object is returned. If the current node is not read-only, the same object is returned.


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
Windows Internet Explorer 9.  The '''replaceWholeText''' method is supported only when webpages are displayed in IE9 Standards mode.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182717 Document Object Model (DOM) Level 3 Core Specification], Section 1.2


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/TextNode|TextNode]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}