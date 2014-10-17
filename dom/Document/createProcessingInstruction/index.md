{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs compat table
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Creates a [[dom/ProcessingInstruction|'''processing instruction''']] for an XML parser.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=target
|Data type=String
|Description=The name of the processing instruction.
|Optional=No
}}{{Method Parameter
|Index=1
|Name=data
|Data type=String
|Description=The data for the processing instruction.
|Optional=No
}}
|Method_applies_to=dom/Document
|Example_object_name=document
|Return_value_name=processingInstruction
|Javascript_data_type=DOM Node
|Return_value_description=The created processing instruction.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following  code example demonstrates how to create an XML processing instruction.
|Code=// This example creates the following processing instruction:
//   &lt;?xml-stylesheet type{{=}}"text/css" href{{=}}"style.css"&gt;
var sTarget {{=}} 'xml-stylesheet';
var sData {{=}} 'type{{=}}"text/css" href{{=}}"style.css"';'
var obj {{=}} document.createProcessingInstruction(sTarget, sData);
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=The '''createProcessingInstruction''' method is supported only for XML documents.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 3 Core
|URL=http://www.w3.org/TR/DOM-Level-3-Core/core.html#ID-135944439
|Status=Recommendation
|Relevant_changes=Section 1.4
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}