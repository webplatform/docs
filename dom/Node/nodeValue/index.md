{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Gets or sets the value of a Node, if the type of Node supports it.}}
{{API_Object_Property
|Property_applies_to=dom/Node
|Read_only=No
|Example_object_name=node
|Return_value_name=value
|Javascript_data_type=String
|Return_value_description=The value of the node.
|Example_value_name=newValue
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following code example alters the text of the specified list item by setting the '''nodeValue''' property of the text node that is contained by that list item.
|Code=&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;head&gt;
&lt;title&gt;Title&lt;/title&gt;
&lt;script&gt;
function changeValue(list, itemIndex, newValue){
   // only perform the operation on lists
   if (list.nodeName !{{=}}{{=}} "UL" &amp;&amp; list.nodeName !{{=}} "OL")
      return false;
   // only perform the operation if the specified index is 
   // within the acceptable range of available list items
   if (itemIndex &gt; list.childNodes.length -1)
      return false;
   // get a reference to the specified list item
   var liElements {{=}} list.childNodes[itemIndex];
   if (!liElements)
      return false;
   // get a reference to the text node contained by the list item
   var textNode {{=}} liElements.childNodes[0];
   // ensure that the node is a text node
   if (textNode.nodeType !{{=}}{{=}} 3)
      return false;
   textNode.nodeValue {{=}} newValue;
   return true;
}
function initialize() {
  document.getElementById("list").addEventListener(
    "click",
    function () {
     changeValue(this, 0, "New Node value");
    },
    false);
}
document.addEventListener("DOMContentLoaded", initialize, false);
&lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;ul id{{=}}"list"&gt;&lt;li&gt;Old Node Value&lt;/li&gt;&lt;/ul&gt;
&lt;/body&gt;
}}
}}
{{Notes_Section
|Usage=Use this property to get or set the value of a Node. The concept of nodeValue changes between the various Node types ([[dom/Element|Element]], [[dom/Text|Text]] and the rest).
|Notes=* The value of this property for [[dom/Text|Text] nodes is their [[dom/Node/textContent|Text.textContent]].
* This property is deprecated for [[dom/Attr|Attr]] nodes. Use [[dom/Attr/value|Attr.value]] instead. The value of this property for Attr nodes is their Attr.value.
* The value of this property for [[dom/Element|Element]] nodes is always <code>null</code>. Use [[dom/Node/nodeName|Node.nodeName]] to get their name or [[dom/Node/textContent]] to get all of the text included in their tree.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 3 Core
|URL=http://www.w3.org/TR/DOM-Level-3-Core/
|Status=W3C Recommendation
}}{{Related Specification
|Name=WHATWG DOM
|URL=http://dom.spec.whatwg.org/#dom-node-nodevalue
|Status=Living Standard
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Node.nodeValue Node.nodeValue]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms534192(v=vs.85).aspx nodeValue Property]
|HTML5Rocks_link=
}}