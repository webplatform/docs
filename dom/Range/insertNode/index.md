{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs some more content.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Inserts a Node into the start of a Range object.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=oNode
|Data type=DOM Node
|Description=The new node to insert.
|Optional=No
}}
|Method_applies_to=dom/Range
|Example_object_name=newNode
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=var range {{=}} document.createRange();
newNode {{=}} document.createElement("p");
newNode.appendChild(document.createTextNode("New Node Inserted Here"));
range.selectNode(document.getElementsByTagName("div").item(0));
range.insertNode(newNode);
}}
}}
{{Notes_Section
|Notes=If the container is a node of type [[dom/Text|'''Text''']], '''insertNode''' splits the text node, and inserts ''newNode'' between the resulting two text nodes.
If ''newNode'' is a document fragment, the children of the document fragment node are inserted rather than the ''newNode'' itself.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM
|URL=http://dom.spec.whatwg.org/#dom-range-insertnode
|Status=Living Standard
}}{{Related Specification
|Name=Document Object Model (DOM) Level 2 Traversal and Range
|URL=http://www.w3.org/TR/DOM-Level-2-Traversal-Range/ranges.html#Level2-Range-method-insertNode
|Status=W3C Recommendation
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Range.insertNode Range.insertNode]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff975445(v=vs.85).aspx insertNode Method]
|HTML5Rocks_link=
}}