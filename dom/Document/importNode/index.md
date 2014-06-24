{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs compat tables
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Imports a node from another document into the the document that the '''document''' object displays.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=node
|Data type=DOM Node
|Description=The node tomove.
|Optional=No
}}{{Method Parameter
|Index=1
|Name=deep
|Data type=Boolean
|Description=Whether child nodes of the node specified by the ''node'' parameter are also imported.
|Optional=Yes
}}
|Method_applies_to=dom/Document
|Example_object_name=document
|Return_value_name=importedNode
|Javascript_data_type=DOM Node
|Return_value_description=The node node that has been imported, or a null if the node cannot be imported.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following  code example illustrates the '''importNode''' method.
|Code=var oNode {{=}} document.importNode( oXHTMLNode, false);
parent.appendChild( oNode );
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 4
|URL=http://www.w3.org/TR/2014/CR-dom-20140508/#dom-document-importnode
|Status=Candidate Recommendation
|Relevant_changes=Changed the parameters to 'node' and 'deep'
}}{{Related Specification
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
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}