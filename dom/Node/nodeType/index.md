{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Retrieves the type of the requested node.}}
{{API_Object_Property
|Property_applies_to=dom/Node
|Read_only=Yes
|Example_object_name=node
|Return_value_name=nodeType
|Javascript_data_type=Number
|Return_value_description=One of the node type constants defined on [[dom/Node|Node]], or null.
Node.ELEMENT_NODE {{=}}1
Node.ATTRIBUTE_NODE {{=}} 2
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=This example assigns the '''nodeType''' property of the '''body''' object to a variable.
|Code=var iType {{=}} document.body.nodeType;
}}{{Single Example
|Language=JavaScript
|Description=This example assigns the '''nodeType''' property of a node created with the [[dom/Document/createElement|'''createElement''']] method to a variable.
|Code=var oNode {{=}} document.createElement("B");
document.body.insertBefore(oNode);
var iType {{=}} oNode.nodeType;
}}{{Single Example
|Language=JavaScript
|Description=This example users the node constants to return the nodeType description.
|Code=function getNodeTypeName(nType){
   switch (nType){
   		case Node.ELEMENT_NODE:
   			return 'ELEMENT_NODE';
   		case Node.ATTRIBUTE_NODE:
   			return 'ATTRIBUTE_NODE';
   		case Node.TEXT_NODE:
   			return 'TEXT_NODE';
   		case Node.CDATA_SECTION_NODE:
   			return 'CDATA_SECTION_NODE';
   		case Node.ENTITY_REFERENCE_NODE:
   			return 'ENTITY_REFERENCE_NODE';
   		case Node.ENTITY_NODE:
   			return 'ENTITY_NODE';
   		case Node.PROCESSING_INSTRUCTION_NODE:
   			return 'PROCESSING_INSTRUCTION_NODE';
   		case Node.COMMENT_NODE:
   			return 'COMMENT_NODE';
   		case Node.DOCUMENT_NODE:
   			return 'DOCUMENT_NODE';
   		case Node.DOCUMENT_TYPE_NODE:
   			return 'DOCUMENT_TYPE_NODE';
   		case Node.DOCUMENT_FRAGMENT_NODE:
   			return 'DOCUMENT_FRAGMENT_NODE';
   		case Node.NOTATION_NODE:
   			return 'NOTATION_NODE';
   		default:
   			return 'unknown nodeType:'+ntype;
      }
   }
}}
}}
{{Notes_Section
|Notes=If the node represents an attribute retrieved from the [[dom/Node/attributes|'''attributes''']] collection, the '''nodeType''' returns <code>null</code>.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 3 Core
|URL=http://www.w3.org/TR/DOM-Level-3-Core/
|Status=Recommendation
|Relevant_changes=Section 1.4
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Node.nodeType Node.nodeType]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms534191(v=vs.85).aspx nodeType Property]
|HTML5Rocks_link=
}}