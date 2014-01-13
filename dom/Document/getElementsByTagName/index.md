{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Gets a collection of all descendant elements with a given name.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=name
|Data type=String
|Description=The name of an element.
|Optional=No
}}
|Method_applies_to=dom/HTMLElement
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=A DOM collection of elements with the given name.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following example uses the '''getElementsByTagName''' method to return the children of a '''ul''' element based on the selected '''li''' element.
|Code=&lt;!doctype html&gt;
&lt;html&gt;
 &lt;head&gt;
  &lt;script&gt;
function printFirstLIText(e){
  var oWorkItem = event.target;
  var aReturn = oWorkItem.parentElement.getElementsByTagName("LI");
  console.log("Length: " + aReturn.length + "\nFirst Item: " +
   aReturn[0].childNodes[0].nodeValue);
}
function initialize() {
  document.getElementById("ex").addEventListener("click", printFirstLIText, false);
}
window.addEventListener("load", initialize, false);
  &lt;/script&gt;
 &lt;/head&gt;
 &lt;body&gt;
  &lt;ul id="ex"&gt;
   &lt;li&gt;Item 1
    &lt;ul&gt;
     &lt;li&gt;Sub Item 1.1
      &lt;ol&gt;
       &lt;li&gt;Super Sub Item 1.1&lt;/li&gt;
       &lt;li&gt;Super Sub Item 1.2&lt;/li&gt;
      &lt;/ol&gt;
     &lt;/li&gt;
     &lt;li&gt;Sub Item 1.2&lt;/li&gt;
     &lt;li&gt;Sub Item 1.3&lt;/li&gt;
    &lt;/ul&gt;
   &lt;/li&gt;	
   &lt;li&gt;Item 2
    &lt;ul&gt;
     &lt;li&gt;Sub Item 2.1
     &lt;li&gt;Sub Item 2.3
    &lt;/ul&gt;
   &lt;/li&gt;
   &lt;li&gt;Item 3&lt;/li&gt;
  &lt;/ul&gt;
 &lt;/body&gt;
&lt;/html&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/getElementsByTagName.htm
}}
}}
{{Notes_Section
|Usage=Use this method to get a collection of all child and nested child elements with the specified tag name.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 2 HTML
|URL=http://www.w3.org/TR/DOM-Level-2-HTML/
|Status=Recommendation
|Relevant_changes=Section 1.6.5
}}
}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
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
*<code>custom</code>
*<code>dd</code>
*<code>del</code>
*<code>dfn</code>
*<code>dir</code>
*<code>div</code>
*<code>dl</code>
*<code>[[dom/Document|Document]]</code>
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
*<code>ol</code>
*<code>p</code>
*<code>plainText</code>
*<code>pre</code>
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