{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=waiting for property and method descriptions to fill description fields... Not sure if all properties and methods have been listed.
Missing document.createTreeWalker method.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Provides an object that can be used to traverse filtered lists of nodes or elements in a document.}}
{{API_Object}}
{{Examples_Section
|Not_required=Yes
|Examples={{Single Example
|Language=JavaScript
|Code=&lt;div id{{=}}"contentarea"&gt;
&lt;p&gt;Some &lt;span&gt;text&lt;/span&gt;&lt;/p&gt;
&lt;b&gt;Bold text&lt;/b&gt;
&lt;/div&gt;

&lt;script type{{=}}"text/javascript"&gt;

var rootnode{{=}}document.getElementById('contentarea');
var walker{{=}}document.createTreeWalker(rootnode, NodeFilter.SHOW_ELEMENT, null, false);

//Alert the starting node Tree Walker currently points to (root node)
alert(walker.currentNode.tagName); //alerts DIV (with id{{=}}contentarea)

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
The '''TreeWalker''' is dynamic, reflecting the state of the document as it is edited or changed.
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182712 Document Object Model (DOM) Level 2 Traversal and Range Specification], Section 1.2
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM
|URL=http://dom.spec.whatwg.org/#treeWalker
|Status=Living Standard
|Relevant_changes=Removed the expandEntityReferences proptery
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/TreeWalker TreeWalker]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff974360(v=vs.85).aspx TreeWalker Object]
|HTML5Rocks_link=
}}