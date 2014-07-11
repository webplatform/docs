{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Retrieves the document object associated with the node.}}
{{API_Object_Property
|Property_applies_to=dom/Node
|Read_only=No
|Return_value_name=doc
|Javascript_data_type=DOM Node
|Return_value_description=The document Node of the web page or iframe or frame.

The document object returned by this property is the main object with which all the child nodes in the actual HTML document are created. If this property is used on a node that is itself a document, the result is null.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Code=// given a node "p", get the top-level HTML child 
// of the document object

var doc {{=}} p.ownerDocument; 
alert(doc.outerHTML);
var html {{=}} doc.documentElement;
alert(html.outerHTML);
}}
}}
{{Notes_Section
|Usage=Used to build the DOM tree of documents that contain &lt;iframe&gt;, &lt;frame&gt; and &lt;frameset&gt; elements.
|Notes====Remarks===
The '''ownerDocument''' is the [[dom/Document|Document]] object that is used to create new nodes.
This property returns null when the node is a [[dom/Document|Document]].
'''ownerDocument''' was introduced in Microsoft Internet Explorer 6.


|Import_Notes====Syntax===
var doc=element.ownerDocument;

}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 2 Core
|URL=http://www.w3.org/TR/2000/REC-DOM-Level-2-Core-20001113/core.html#node-ownerDoc
|Status=Recommendation
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Node.ownerDocument Node.ownerDocument]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms534315(v=vs.85).aspx ownerDocument Property]
|HTML5Rocks_link=
}}