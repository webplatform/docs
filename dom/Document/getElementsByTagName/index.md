{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=v|Data type=BSTR|Description='''String''' that specifies the name of an element.|Optional=}}
|Method_applies_to=dom/HTMLElement
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description='''IHTMLElementCollection'''


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example uses the '''getElementsByTagName''' method to return the children of a '''ul''' element based on the selected '''li''' element.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/getElementsByTagName.htm
|Code=
&lt;SCRIPT&gt;
function fnGetTags(){
   var oWorkItem{{=}}event.srcElement;
   var aReturn{{=}}oWorkItem.parentElement.getElementsByTagName("LI");
   alert("Length: "
      + aReturn.length
      + "\nFirst Item: "
      + aReturn[0].childNodes[0].nodeValue);
}
&lt;/SCRIPT&gt;
&lt;UL onclick{{=}}"fnGetTags()"&gt;
&lt;LI&gt;Item 1
   &lt;UL&gt;
      &lt;LI&gt;Sub Item 1.1
      &lt;OL&gt;
         &lt;LI&gt;Super Sub Item 1.1
         &lt;LI&gt;Super Sub Item 1.2
      &lt;/OL&gt;
      &lt;LI&gt;Sub Item 1.2
      &lt;LI&gt;Sub Item 1.3
   &lt;/UL&gt;		
&lt;LI&gt;Item 2
   &lt;UL&gt;
      &lt;LI&gt;Sub Item 2.1
      &lt;LI&gt;Sub Item 2.3
   &lt;/UL&gt;
&lt;LI&gt;Item 3
&lt;/UL&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''getElementsByTagName''' method is equivalent to using the [[dom/methods/tags|'''tags''']] method on the [[dom/properties/all|'''all''']] collection. For example, the following code shows how to retrieve a collection of '''div''' elements from the '''body''' element, first using the Dynamic HTML (DHTML) Object Model and then the Document Object Model (DOM).
*Using the DHTML Object Model: <div class{{=}}"codeSnippet">
<pre xml:space{{=}}"preserve"><code>var aDivs {{=}} document.body.all.tags("DIV");</code></pre>
</div>
*Using the DOM: <div class{{=}}"codeSnippet">
<pre xml:space{{=}}"preserve"><code>var aDivs {{=}} document.body.getElementsByTagName("DIV");</code></pre>
</div>

When you use the '''getElementsByTagName''' method, all child and nested child elements with the specified tag name are returned. 

For example, all of the '''SPAN''' elements in the following example would be returned by the '''getElementsByTagName''' method.
 <code>
 &lt;SCRIPT&gt;
 var aSpans {{=}} oDiv.getElementsByTagName("SPAN");
 &lt;/SCRIPT&gt;
 &lt;DIV id{{=}}"oDiv"&gt;
     &lt;SPAN&gt;Immediate Child
         &lt;DIV&gt;
             &lt;SPAN&gt;Child of Child DIV&lt;/SPAN&gt;
         &lt;/DIV&gt;
     &lt;/SPAN&gt;
 &lt;/DIV&gt;
 </code>
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}196991 Document Object Model (DOM) Level 2 HTML Specification], Section 1.6.5


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
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
*<code>[[dom/document|document]]</code>
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
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}