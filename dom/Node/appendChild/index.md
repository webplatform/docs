{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Appends an element as a child to the object.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=newChild
|Data type=DOM Node
|Description=The child to append.
|Optional=No
}}
|Method_applies_to=dom/Node
|Example_object_name=node
|Return_value_name=appendedChild
|Javascript_data_type=DOM Node
|Return_value_description=The appended child.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''appendChild''' method to add an item to an unordered list.
|Code=&lt;!doctype html&gt;
&lt;script&gt;
function fnAppend(){
   var oNewNode {{=}} document.createElement("LI");
   oList.appendChild(oNewNode);
   oNewNode.innerText{{=}}"List node 5";
}
&lt;/script&gt;
&lt;body&gt;
&lt;ul ID {{=}} oList&gt;
&lt;li&gt;List node 1&lt;/li&gt;
&lt;li&gt;List node 2&lt;/li&gt;
&lt;li&gt;List node 3&lt;/li&gt;
&lt;li&gt;List node 4&lt;/li&gt;
&lt;/ul&gt;
&lt;input
   type {{=}} "button"
   value {{=}} "Append Child"
   onclick {{=}} "fnAppend()" /&gt;
&lt;/body&gt;
}}
}}
{{Notes_Section
|Usage=Use this method to append elements to the end of the [[dom/Node/childNodes|'''childNodes''']] collection.
|Notes=To display new elements on the page, you must append them within the '''body''' element. For example, the following syntax demonstrates how to add a '''div''' element to the '''body'''.
 <code>var oDiv{{=}}document.createElement("DIV");
 document.body.appendChild(oDiv);</code>
This method is accessible at run time. If elements are removed at run time, before the closing tag is parsed, areas of the document might not render.
Windows Internet Explorer 9. Exceptions are only supported when webpages are displayed in IE9 Standards mode.
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
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=6
|Note=This method applies to the [[dom/HTMLElement/attribute|'''attribute''']] object.
}}
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