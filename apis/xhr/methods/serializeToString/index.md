{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=pNode|Data type=IHTMLDOMNode|Description=The parent DOM node of a document tree to convert to an XML string.|Optional=}}
|Method_applies_to=apis/xhr/objects/XMLSerializer
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=String

The string that contains an XML representation of a DOM node tree.


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
To use the '''serializeToString''' method, type the following syntax.
 <code>oXmlSerializer {{=}}  new XMLSerializer();
 sXmlString {{=}} oXmlSerializer.serializeToString(oDOMNode);</code>
|Import_Notes=
===Syntax===
===Standards information===
There are no standards that apply here.

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[apis/xhr/objects/XMLSerializer|XMLSerializer]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}