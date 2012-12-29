{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Returns the value of the content attribute.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=name
|Data type=String
|Description=The name of the attribute.
|Optional=No
}}
|Method_applies_to=dom/HTMLElement
|Example_object_name=element
|Return_value_name=attributeValue
|Javascript_data_type=String
|Return_value_description=The value of the attribute, or null if it does not exist.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following example shows the difference between a URL attribute which is using a content attribute (value from '''getAttribute''') and a DOM attribute (property).
|Code=&lt;!doctype html&gt;
&lt;head&gt;
  &lt;title&gt;Content/DOM Attribute Example&lt;/title&gt;
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
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/getAttribute8.htm
}}
}}
{{Notes_Section
|Notes=If two or more attributes have the same name, this method retrieves values only for the last attribute created with this name, and ignores all other attributes with the same name.
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
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=7 and earlier
|Note=The '''name''' parameter requires the name of the desired DOM attribute ("className", for example) and not the content attribute ("class").
}}{{Compatibility Notes Row
|Browser=Internet Explorer
|Version=7 and earlier
|Note=Boolean attributes (like <code>&lt;input readonly disabled&gt;</code> and such) return a Boolean value, instead of their names ("readonly", "disabled").
}}{{Compatibility Notes Row
|Browser=Internet Explorer
|Version=7 and earlier
|Note=There is an optional '''flag''' parameter that accepts one of the following values - <code>0</code> (default) - case insensitive attribute name search. 1 - case sensitive attribute name search. 2 - return the value as a string (as opposed to Boolean). 4 - return the value as a fully expanded URL, which only works for URL attributes such as [[html/attributes/action|'''action''']],  [[html/attributes/background (Body element)|'''background''']],  [[html/attributes/BaseHref|'''BaseHref''']],  [[html/attributes/cite|'''cite''']],  [[html/attributes/codeBase|'''codeBase''']],  [[html/attributes/data|'''data''']],  '''dynsrc''',  [[html/attributes/href|'''href''']],  [[html/attributes/longDesc|'''longDesc''']],  [[html/attributes/lowsrc|'''lowsrc''']],  [[html/attributes/pluginspage|'''pluginspage''']],  '''profile''',  [[html/attributes/src (input, img)|'''src''']],  [[dom/properties/vrml|'''vrml''']].
}}{{Compatibility Notes Row
|Browser=Internet Explorer
|Version=7 and earlier
|Note=The '''name''' parameter value is case sensitive.
}}{{Compatibility Notes Row
|Browser=Internet Explorer
|Version=7 and earlier
|Note=Content/DOM URL attributes return a fully qualified/relative URL and not the original content attribute value.
}}
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
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
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}