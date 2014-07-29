{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Sets or retrieves where the current node in a filtered TreeWalker hierarchy is positioned.}}
{{API_Object_Property
|Property_applies_to=dom/TreeWalker
|Read_only=No
|Example_object_name=walker
|Return_value_name=node
|Javascript_data_type=DOM Node
|Return_value_description=The currentNode of the TreeWalker object.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Code=&lt;div id{{=}}"divcontent"&gt;
&lt;p&gt;Some &lt;span&gt;text&lt;/span&gt;&lt;/p&gt;
&lt;b&gt;Bold text&lt;/b&gt;
&lt;/div&gt;

&lt;script type{{=}}"text/javascript"&gt;

var rootnode{{=}}document.getElementById('divcontent');
var walker{{=}}document.createTreeWalker(rootnode, NodeFilter.SHOW_ELEMENT, null, false);

//Alert the starting node Tree Walker currently points to (root node)
alert(walker.currentNode.tagName) //alerts DIV (with id{{=}}divcontent)

//Step through and alert all child nodes
while (walker.nextNode())
alert(walker.currentNode.tagName) //alerts P, SPAN, and B.

//Go back to the first child node of the collection and alert it
walker.currentNode{{=}}rootnode; //reset TreeWalker pointer to point to root node
alert(walker.firstChild().tagName); //alerts P

&lt;/script&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
'''currentNode''' will never return null in Windows Internet Explorer 9, even when the traversing method returns null.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182712 Document Object Model (DOM) Level 2 Traversal and Range Specification], Section 1.2
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM
|URL=http://dom.spec.whatwg.org/#dom-treewalker-currentnode
|Status=Living Standard
|Relevant_changes=No Change
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/TreeWalker.currentNode TreeWalker.currentNode]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff974804(v=vs.85).aspx currentNode Property]
|HTML5Rocks_link=
}}