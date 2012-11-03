{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Gets or sets the value of a node.}}
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
|Code=&lt;script&gt;
function fnChangeValue(oList, iItem, sValue){
   // only perform the operation on lists
   if (oList.nodeName !{{=}} "UL" &amp;&amp; oList.nodeName !{{=}} "OL")
      return false;
   // only perform the operation if the specified index is 
   // within the acceptable range of available list items
   if (iItem &gt; oList.childNodes.length -1)
      return false;
   // get a reference to the specified list item
   var oLI {{=}} oList.childNodes(i);
   if (!oLI)
      return false;
   // get a reference to the text node contained by the list item
   var oText {{=}} oLI.childNodes(0);
   // ensure that the node is a text node
   if (oText.nodeType !{{=}} 3)
      return false;
   oText.nodeValue {{=}} sValue;
   return true;
}
&lt;/script&gt;
&lt;ul id{{=}}"oList" onclick{{=}}"fnChangeValue(this, 0, 'New Node value')"&gt;
&lt;li&gt;Old Node Value&lt;/li&gt;
&lt;/ul&gt;
}}
}}
{{Notes_Section
|Notes=If the object is a [[dom/TextNode|'''TextNode''']] object, the '''nodeValue''' property returns a string that represents the text that the node contains.
You cannot use expressions to change the '''nodeValue''' of a [[dom/TextNode|'''TextNode''']] object.
If the object is an [[dom/attributes|'''attribute''']] object retrieved from the [[dom/properties/attribute|'''attributes''']] collection, the '''nodeValue''' property returns the value of the attribute if it has been specified, or <code>null</code> otherwise.
If the object is an element, the '''nodeValue''' returns <code>null</code>. Use the [[dom/properties/nodeName|'''nodeName''']] property to determine the element name.
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
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[html/elements/a|a]]</code>
*<code>abbr</code>
*<code>[[html/elements/acronym|acronym]]</code>
*<code>address</code>
*<code>applet</code>
*<code>area</code>
*<code>[[dom/attributes|attribute]]</code>
*<code>b</code>
*<code>base</code>
*<code>baseFont</code>
*<code>bdo</code>
*<code>bgSound</code>
*<code>big</code>
*<code>blockQuote</code>
*<code>body</code>
*<code>br</code>
*<code>button</code>
*<code>caption</code>
*<code>center</code>
*<code>cite</code>
*<code>code</code>
*<code>col</code>
*<code>colGroup</code>
*<code>comment</code>
*<code>dd</code>
*<code>del</code>
*<code>dfn</code>
*<code>dir</code>
*<code>div</code>
*<code>dl</code>
*<code>[[dom/documentType|documentType]]</code>
*<code>dt</code>
*<code>em</code>
*<code>embed</code>
*<code>fieldSet</code>
*<code>font</code>
*<code>form</code>
*<code>frame</code>
*<code>frameSet</code>
*<code>head</code>
*<code>hn</code>
*<code>hr</code>
*<code>html</code>
*<code>i</code>
*<code>iframe</code>
*<code>img</code>
*<code>input type{{=}}button</code>
*<code>input type{{=}}checkbox</code>
*<code>input type{{=}}file</code>
*<code>input type{{=}}hidden</code>
*<code>input type{{=}}image</code>
*<code>input type{{=}}password</code>
*<code>input type{{=}}radio</code>
*<code>input type{{=}}reset</code>
*<code>input type{{=}}submit</code>
*<code>input type{{=}}text</code>
*<code>ins</code>
*<code>kbd</code>
*<code>label</code>
*<code>legend</code>
*<code>li</code>
*<code>link</code>
*<code>listing</code>
*<code>map</code>
*<code>marquee</code>
*<code>menu</code>
*<code>[[html/elements/nextID|nextID]]</code>
*<code>object</code>
*<code>ol</code>
*<code>option</code>
*<code>p</code>
*<code>plainText</code>
*<code>pre</code>
*<code>[[dom/processingInstruction|ProcessingInstruction]]</code>
*<code>q</code>
*<code>s</code>
*<code>samp</code>
*<code>script</code>
*<code>select</code>
*<code>small</code>
*<code>span</code>
*<code>strike</code>
*<code>strong</code>
*<code>sub</code>
*<code>sup</code>
*<code>[[html/elements/table|table]]</code>
*<code>tBody</code>
*<code>td</code>
*<code>textArea</code>
*<code>[[dom/TextNode|TextNode]]</code>
*<code>tFoot</code>
*<code>th</code>
*<code>tHead</code>
*<code>title</code>
*<code>tr</code>
*<code>tt</code>
*<code>u</code>
*<code>ul</code>
*<code>var</code>
*<code>xmp</code>
*<code>Reference</code>
*<code>[[dom/properties/value|value]]</code>
*<code>Conceptual</code>
*<code>About the W3C Document Object Model</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}