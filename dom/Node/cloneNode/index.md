{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Copies a reference to the object from the document hierarchy.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=cloneDescendants
|Data type=Boolean
|Description=Whether to clone the child nodes of the node as well.
|Optional=No
}}
|Method_applies_to=dom/Node
|Example_object_name=node
|Return_value_name=clonedNode
|Javascript_data_type=DOM Node
|Return_value_description=The cloned node.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Code=&lt;!doctype html&gt;
&lt;script&gt;
function fnClone(){
   /* the 'true' possible value specifies to clone
      the childNodes as well.
   */
   var oCloneNode {{=}} document.getElementById("oList").cloneNode(true);
   /* When the cloned node is added,
   'oList' becomes a collection.
   */
   document.body.insertBefore(oCloneNode);
}
&lt;/script&gt;
&lt;ul id{{=}}"oList"&gt;
&lt;li&gt;List node 1&lt;/li&gt;
&lt;li&gt;List node 2&lt;/li&gt;
&lt;li&gt;List node 3&lt;/li&gt;
&lt;li&gt;List node 4&lt;/li&gt;
&lt;/ul&gt;
&lt;input type{{=}}"button" value{{=}}"Clone List" onclick{{=}}"fnClone()"&gt;
}}
}}
{{Notes_Section
|Usage=Use this method to copy an node, its attributes and, if specified, its [[dom/Node/childNodes|'''childNodes''']] as well.
|Notes=When you refer to the '''id''' of a cloned element, a collection is returned. 
'''cloneNode'''does not work on an '''IFRAME''' directly. You must call '''cloneNode'''through the '''all''' collection. The following example demonstrates how to call '''cloneNode''' on an '''iframe'''.
 <code>&lt;!doctype html&gt;
&lt;html&gt;
 &lt;script&gt;
 function fnBegin(){
     var fr {{=}} document.getElementByid("oFrame").cloneNode();
     console.log(document.body.innerHTML);
 }    
 &lt;/script&gt;
 &lt;body onload{{=}}"fnBegin()"&gt;
     &lt;iframe id{{=}}"oFrame" src{{=}}"about:blank" 
         style{{=}}"border:1px solid black; position:absolute; top:20px; left:30px;
             width:350px; height:300px;"&gt;&lt;/iframe&gt;
 &lt;/body&gt;    
 &lt;/html&gt;</code>
If the object being cloned is an element and that element has expandos defined on it, the expandos are copied to the clone when '''cloneNode''' is called.  Other browsers might handle this differently.
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Node.cloneNode Node.cloneNode]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms536365(v=vs.85).aspx cloneNode Method]
|HTML5Rocks_link=
}}