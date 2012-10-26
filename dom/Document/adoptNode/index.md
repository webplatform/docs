{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Tries to move a node from one document to the document that the '''document''' object displays.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=element
|Data type=DOM Node
|Description=The element to move.
|Optional=No
}}
|Method_applies_to=dom/document
|Example_object_name=document
|Return_value_name=element
|Javascript_data_type=DOM Node
|Return_value_description=The node that has been moved, or a null value if the node cannot be moved.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following  code example illustrates the '''adoptNode''' method and  shows one way to handle cases where the method fails.
|Code=var oNode {{=}} document.adoptNode( oXHTMLNode );
if ( oNode {{=}}{{=}} null )
   oNode {{=}} document.importNode( oXHTMLNode );
parent.appendChild( oNode );
}}
}}
{{Notes_Section}}
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
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/document|document]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}