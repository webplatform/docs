{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=bstrTarget|Data type=BSTR|Description=A '''String''' value  that contains  the name of the processing instruction.|Optional=}}
{{Method Parameter|Name=bstrData|Data type=BSTR|Description=A '''String''' value  that contains  the data for the processing instruction.|Optional=}}
{{Method Parameter|Name=newProcessingInstruction|Data type=IDOMProcessingInstruction|Description=|Optional=}}
|Method_applies_to=dom/document
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

This method can return one of these values.

{| class="wikitable"
|-
!Return code
!Description
|-
|S_OK
|The operation completed successfully.
|}
 

'''IDOMProcessingInstruction'''


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following  code example demonstrates how to create an XML processing instruction.
|LiveURL=
|Code=
// This example creates the following processing instruction:
//   &lt;?xml-stylesheet type{{=}}"text/css" href{{=}}"style.css"&gt;
var sTarget {{=}} 'xml-stylesheet';
var sData {{=}} 'type{{=}}"text/css" href{{=}}"style.css"';'
var obj {{=}} document.createProcessingInstruction( sTarget, sData );

}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''createProcessingInstruction''' method is supported only for XML documents.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182717 Document Object Model (DOM) Level 3 Core Specification], Section 1.4


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/document|document]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}