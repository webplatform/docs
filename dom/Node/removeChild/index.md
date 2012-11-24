{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Removes a child node from a node.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=oldChild
|Data type=Blob
|Description=The node to be removed from the document.
|Optional=No
}}
|Method_applies_to=dom/Node
|Example_object_name=node
|Return_value_name=removedNode
|Javascript_data_type=DOM Node
|Return_value_description=The removed node.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''removeChild''' method to remove a bold element from a '''div'''.
|Code=&lt;!doctype html&gt;
&lt;head&gt;
&lt;script&gt;
function removeElement()
{
  var div1 = document.getElementById("Div1");
  try
  {
      //The first child of the div is the bold element.
    var oChild{{=}}div1.children(0);	
    div1.removeChild(oChild);
  }
  catch(x)
  {
    alert("You have already removed the bold element.\nPage will be refreshed when you click OK.")
    document.location.reload();
  }
}
&lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;div id{{=}}"Div1" onclick{{=}}"removeElement()"&gt;
Click anywhere in this sentence to remove this &lt;strong&gt;Bold&lt;/strong&gt; word.
&lt;/div&gt;
&lt;/body&gt;
}}
}}
{{Notes_Section
|Notes=The node to be removed must be an immediate child of the parent node.
This method is accessible at run time. If elements are removed at run time, before the closing tag is parsed, areas of the document might not render.
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
|Version=9
|Note=Exceptions are supported
}}{{Compatibility Notes Row
|Browser=Internet Explorer
|Version=6
|Note=This method also applies to the [[dom/attributes|'''attribute''']] object.
}}
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[html/elements/a|a]]</code>
*<code>abbr</code>
*<code>[[html/elements/acronym|acronym]]</code>
*<code>address</code>
*<code>[[dom/attributes|attribute]]</code>
*<code>b</code>
*<code>bdo</code>
*<code>big</code>
*<code>blockQuote</code>
*<code>body</code>
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
*<code>fieldSet</code>
*<code>font</code>
*<code>form</code>
*<code>frameSet</code>
*<code>head</code>
*<code>hn</code>
*<code>html</code>
*<code>i</code>
*<code>iframe</code>
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
*<code>listing</code>
*<code>map</code>
*<code>marquee</code>
*<code>menu</code>
*<code>[[html/elements/nextID|nextID]]</code>
*<code>ol</code>
*<code>option</code>
*<code>p</code>
*<code>plainText</code>
*<code>pre</code>
*<code>[[dom/processingInstruction|ProcessingInstruction]]</code>
*<code>q</code>
*<code>s</code>
*<code>samp</code>
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
*<code>tFoot</code>
*<code>th</code>
*<code>tHead</code>
*<code>tr</code>
*<code>tt</code>
*<code>u</code>
*<code>ul</code>
*<code>var</code>
*<code>xmp</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}