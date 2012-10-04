{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=v|Data type=BSTR|Description=A '''String''' that specifies the ID value. Case-insensitive.|Optional=}}
|Method_applies_to=dom/document
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description='''IHTMLElement'''

'''ID'''

'''NAME'''


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example uses '''getElementById''' to display the content of the first '''div''' element in a collection with the [[html/attributes/id|'''ID''']] attribute value, <code>oDiv1</code>, when a button is clicked.
|LiveURL=
|Code=
&lt;!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd"&gt;
&lt;html&gt;
&lt;head&gt;
  &lt;title&gt;"Show First DIV Content"&lt;/title&gt;
  &lt;meta http-equiv{{=}}"Content-Type" content{{=}}"text/html; charset{{=}}utf-8" &gt;
  &lt;meta http-equiv{{=}}"X-UA-Compatible" content{{=}}"IE{{=}}8"&gt;
&lt;script type{{=}}"text/javascript"&gt;
function fnGetId(){
   // Display the content of the first DIV element in the collection.
   var oVDiv{{=}}document.getElementById("oDiv1");
   alert("The content of the first DIV element is " + "\"" + oVDiv.innerHTML + "\".");
}
&lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
  &lt;div id{{=}}"oDiv1"&gt;Div #1&lt;/div&gt;
  &lt;div id{{=}}"oDiv2"&gt;Div #2&lt;/div&gt;
  &lt;div id{{=}}"oDiv3"&gt;Div #3&lt;/div&gt;
  &lt;input type{{=}}"button" value{{=}}"Show First DIV Content" onclick{{=}}"fnGetId()"&gt; 
&lt;/body&gt;
&lt;/html&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
If more than one element is found, '''getElementById''' returns the first object in the collection.
Windows Internet Explorer 8 and later. In IE8 Standards mode, '''getElementById''' performs a case-sensitive match on the [[html/attributes/id|'''ID''']] attribute only. In IE7 Standards mode and previous modes, this method performs a case-insensitive match on both the '''ID''' and [[html/attributes/name|'''NAME''']] attributes, which might produce unexpected results. For more information, see Defining Document Compatibility.
Internet Explorer 8 or later. An alternate implementation is available. For more information, see '''getElementById'''.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182717 Document Object Model (DOM) Level 3 Core Specification], Section 1.4


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/document|document]]</code>
*<code>About the W3C Document Object Model</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}