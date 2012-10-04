{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=strAttributeName|Data type=BSTR|Description='''String''' that specifies the name of the attribute.|Optional=}}
{{Method Parameter|Name=lFlags|Data type=Integer|Description='''Integer''' that specifies one or more of the following flags:|Optional=}}
|Method_applies_to=dom/HTMLElement
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Variant

'''Variant''' that returns a '''String''', '''Variant''' of type '''Integer''', or '''Boolean''' value as defined by the attribute. If the attribute is not present, this method returns null.


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example shows the difference between a URL attribute which is using a content attribute (value from '''getAttribute''') and a DOM attribute (property).
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/getAttribute8.htm
|Code=
&lt;head&gt;
  &lt;meta http-equiv{{=}}"X-UA-Compatible" content{{=}}"IE{{=}}8"&gt;
  &lt;title&gt;Content/DOM Attribute Example&lt;/title&gt;
  &lt;base href{{=}}"http://msdn.microsoft.com/"&gt;
  &lt;script&gt;
    function GetAttr(){
     //Retrieve an element value from the content attribute and DOM attribute.
     var o {{=}} document.getElementById("msdn");
     
     var sContentAttr {{=}} o.getAttribute("href");
     var sDomAttr {{=}} o.href;
     
     var sOutput {{=}} ("Content attribute value: " + sContentAttr + 
              "&lt;br/&gt;DOM attribute value: " + sDomAttr);
     document.getElementById("output").innerHTML {{=}} sOutput;
    }
  &lt;/script&gt;
&lt;/head&gt;
&lt;body onload{{=}}"GetAttr()"&gt;
   &lt;a id{{=}}"msdn" href{{=}}"en-us/default.aspx"&gt;Microsoft Developer Network&lt;/a&gt;
   &lt;div id{{=}}"output"&gt;Output appears here.&lt;/div&gt;
&lt;/body&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
Windows Internet Explorer 8 and later. IE8 Standards mode enables several enhancements to the [[dom/methods/setAttribute|'''setAttribute''']], '''getAttribute''', and [[dom/methods/removeAttribute|'''removeAttribute''']] methods that are not available when pages are displayed in earlier document modes.
*The ''strAttributeName'' parameter requires the name of the desired content attribute and not the Document Object Model (DOM) attribute. 

For example, in IE8 mode, this method no longer requires ''strAttributeName'' to be <code>"className"</code> when setting, getting, or removing a [[dom/properties/className|'''CLASS''']] attribute. Earlier versions of Windows Internet Explorer and Internet Explorer 8 in compatibility mode still require ''strAttributeName'' to specify the corresponding DOM property name.
*The ''strAttributeName'' parameter is not case sensitive. As a result, the ''lFlags'' parameter is no longer supported and should not be used.
*The methods support event handlers. For example, the following code example defines an event handler to call a function called SomeFunction when the body of the page is loaded.
<div class{{=}}"codeSnippet">
<pre xml:space{{=}}"preserve"><code>document.body.setAttribute('onload', 'SomeFunction()');</code></pre>
</div>

Internet Explorer 8 or later. In IE8 mode, the [[dom/properties/value|'''value''']] property is correctly reported as a canonical attribute name. For example, '''&lt;input type{{=}}"text" readonly&gt;''' and '''&lt;input type{{=}}"text" readonly{{=}}"readonly"&gt;''' would both set the input text field to read-only. In IE8 mode, the value is evaluated as a canonical value, <code>"readonly"</code>. In IE7 and earlier modes, it is evaluated as a Boolean value, true. For more information, see Attribute Differences in Internet Explorer 8
If two or more attributes have the same name (differing only in uppercase and lowercase letters) and ''lFlags'' is '''0''', the '''getAttribute''' method retrieves values only for the last attribute created with this name, and ignores all other attributes with the same name.
Internet Explorer 8 and later. In IE7 Standards mode and IE5 (Quirks) mode, attributes that represent URLs and file paths return the same value whether you retrieve them as a DOM property or as a content attribute (using '''getAttribute'''). Some attributes return relative URLs, whereas others always return a fully qualified URL. In IE8 mode, DOM attributes always return fully qualified URLs for URL attributes; to retrieve the attribute value as specified in the content, use '''getAttribute'''. The following attributes return URLs: 
[[html/attributes/action|'''action''']], 
[[html/attributes/background (Body element)|'''background''']], 
[[html/attributes/BaseHref|'''BaseHref''']], 
[[html/attributes/cite|'''cite''']], 
[[html/attributes/codeBase|'''codeBase''']], 
[[html/attributes/data|'''data''']], 
'''dynsrc''', 
[[html/attributes/href|'''href''']], 
[[html/attributes/longDesc|'''longDesc''']], 
[[html/attributes/lowsrc|'''lowsrc''']], 
[[html/attributes/pluginspage|'''pluginspage''']], 
'''profile''', 
[[html/attributes/src (input, img)|'''src''']], 
[[dom/properties/vrml|'''vrml''']].
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}196991 Document Object Model (DOM) Level 2 HTML Specification], Section 1.6.5


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[html/elements/a|a]]</code>
*<code>address</code>
*<code>applet</code>
*<code>area</code>
*<code>b</code>
*<code>base</code>
*<code>baseFont</code>
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
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>custom</code>
*<code>dd</code>
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
*<code>kbd</code>
*<code>label</code>
*<code>legend</code>
*<code>li</code>
*<code>link</code>
*<code>listing</code>
*<code>map</code>
*<code>marquee</code>
*<code>menu</code>
*<code>meta</code>
*<code>[[html/elements/nextID|nextID]]</code>
*<code>noBR</code>
*<code>object</code>
*<code>ol</code>
*<code>option</code>
*<code>p</code>
*<code>plainText</code>
*<code>pre</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
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
*<code>xmp</code>
*<code><b/></code>
*<code>[[dom/methods/removeAttribute|removeAttribute]]</code>
*<code>[[dom/methods/setAttribute|setAttribute]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}