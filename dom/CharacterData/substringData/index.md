{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=offset|Data type=Integer|Description='''Integer''' that specifies the offset from which to start.|Optional=}}
{{Method Parameter|Name=Count|Data type=Integer|Description='''Integer''' that specifies the number of characters to extract.|Optional=}}
|Method_applies_to=dom/TextNode
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=String


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
'''substringData''' was introduced in Microsoft Internet Explorer 6
If the sum of the ''offset'' and ''Count'' parameters exceeds the number of characters in the object, then an error is returned.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182717 Document Object Model (DOM) Level 3 Core Specification], Section 1.4


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>comment</code>
*<code>[[dom/TextNode|TextNode]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}