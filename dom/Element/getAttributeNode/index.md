{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/Element
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.

'''IHTMLDOMAttribute'''

'''attribute'''

'''IHTMLDOMAttribute2'''


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example uses '''getAttributeNode''' to create an [[dom/attributes|'''attribute''']] object and populate its '''div''' element. Note how the call to [[dom/methods/setAttribute|'''setAttribute''']] changes the [[html/attributes/href|'''href''']] value for the content attribute but not for the DOM attribute.
|LiveURL=
|Code=
&lt;html&gt;
&lt;head&gt;
  &lt;meta http-equiv{{=}}"X-UA-Compatible" content{{=}}"IE{{=}}8"&gt;
  &lt;title&gt;Attribute Node Example&lt;/title&gt;
  &lt;base href{{=}}"http://msdn.microsoft.com/"&gt;
  &lt;script&gt;
    function GetAttrNode(){
     //Retrieve an attribute node and a DOM attribute.
     var o {{=}} document.getElementById("msdn");
     var sDomAttr {{=}} o.href;
     
     o.setAttribute('href', 'en-us/ie/default.aspx');
     var sContentAttr {{=}} o.getAttributeNode("href");
     var sOutput {{=}} ("Content attribute node value: " + sContentAttr.value + 
              "&lt;br/&gt;DOM attribute value: " + sDomAttr);
              
     document.getElementById("output").innerHTML {{=}} sOutput;
    }
  &lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
   &lt;a id{{=}}"msdn" href{{=}}"en-us/default.aspx"&gt;Microsoft Developer Network&lt;/a&gt;
   &lt;div id{{=}}"output" onmouseover{{=}}"GetAttrNode()"&gt;Point here to display attribute values.&lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
Windows Internet Explorer 8 or later. In IE8 Standards mode, '''getAttributeNode''' correctly populates the [[dom/properties/value|'''value''']] property of the returned [[dom/attributes|'''attribute''']] object regardless of whether the [[dom/properties/specified|'''specified''']] property is set to true or false. For more information on IE8 mode, see Defining Document Compatibility.
Internet Explorer 8 or later. In IE8 mode, the [[dom/properties/value|'''value''']] property is correctly reported as a canonical attribute name. For example, '''&lt;input type{{=}}"text" readonly&gt;''' and '''&lt;input type{{=}}"text" readonly{{=}}"readonly"&gt;''' would both set the input text field to read-only. In IE8 mode, the value is evaluated as a canonical value, '''"readonly"'''. In IE7 and earlier modes, it is evaluated as a Boolean value, true.
'''getAttributeNode''' was introduced in Microsoft Internet Explorer 6.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182717 Document Object Model (DOM) Level 3 Core Specification], Section 1.4


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
*<code>comment</code>
*<code>custom</code>
*<code>dd</code>
*<code>del</code>
*<code>dfn</code>
*<code>dir</code>
*<code>div</code>
*<code>dl</code>
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
*<code>isIndex</code>
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
*<code>noBR</code>
*<code>noFrames</code>
*<code>noScript</code>
*<code>object</code>
*<code>ol</code>
*<code>option</code>
*<code>p</code>
*<code>plainText</code>
*<code>pre</code>
*<code>q</code>
*<code>rt</code>
*<code>ruby</code>
*<code>s</code>
*<code>samp</code>
*<code>script</code>
*<code>select</code>
*<code>small</code>
*<code>span</code>
*<code>strike</code>
*<code>strong</code>
*<code>[[css/cssom/style|style]]</code>
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
*<code>wbr</code>
*<code>xml</code>
*<code>xmp</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}