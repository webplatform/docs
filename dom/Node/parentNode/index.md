{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Retrieves the parent node in the document hierarchy.}}
{{API_Object_Property
|Property_applies_to=dom/Node
|Read_only=Yes
|Example_object_name=node
|Return_value_name=parentNode
|Javascript_data_type=DOM Node
|Return_value_description=The parent node of the node.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example assigns the '''parentNode''' of a '''span''' object to a variable.
|Code=&lt;script&gt;
var oParent {{=}} document.getElementById("oSpan").parentNode;
&lt;/script&gt;
:
&lt;body&gt;
&lt;span ID{{=}}"oSpan"&gt;A Span&lt;/span&gt;
&lt;/body&gt;
}}{{Single Example
|Language=JavaScript
|Description=This example assigns the '''parentNode''' of a node, created with the [[dom/Document/createElement|'''createElement''']] method, to a variable.
|Code=var oNode {{=}} document.createElement("B");
document.body.insertBefore(oNode);
// This returns document.body.
var oParent {{=}} oNode.parentNode;
}}{{Single Example
|Language=HTML
|Description=This example demonstrates the difference between parentNode and parentElement when queried on the documents root element (&lt;html&gt;)
|Code=&lt;!DOCTYPE html&gt;
&lt;html id{{=}}"root"&gt;

&lt;head&gt;
&lt;meta content{{=}}"text/html; charset=utf-8" http-equiv{{=}}"Content-Type"&gt;
&lt;title&gt;parentElement/parentNode&lt;/title&gt;
&lt;/head&gt;

&lt;body&gt;
&lt;script type{{=}}"text/javascript"&gt;
var root{{=}}document.getElementById('root');
try{document.write('typeof root.parentNode:'+ typeof(root.parentNode)+'<br/>');}catch(e){alert(e);}
try{document.write('root.parentNode.tagName:'+root.parentNode.tagName+'<br/>');}catch(e){alert(e);}
try{document.write('typeof root.parentElement:'+typeof(root.parentElement)+'<br/>');}catch(e){alert(e);}
try{document.write('root.parentElement.tagName:'+root.parentElement.tagName+'<br/>');}catch(e){alert(e);}
&lt;/script&gt;
&lt;/body&gt;

</html>

}}
}}
{{Notes_Section
|Usage=Use to find the parent of a node (if any).
|Notes=The topmost object returns null as its parent.
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Node.parentNode Node.parentNode]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms534328(v=vs.85).aspx parentNode Property]
|HTML5Rocks_link=
}}