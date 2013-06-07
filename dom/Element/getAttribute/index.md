{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
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
|Method_applies_to=dom/Element
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
|Usage=Use this method to get the value of a content attribute of an element.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Document Object Model (DOM) Level 3 Core
|URL=http://www.w3.org/TR/DOM-Level-3-Core/
|Status=Recommendation
|Relevant_changes=Section 1.4
}}{{Related Specification
|Name=Document Object Model (DOM) Level 2 Core
|URL=http://www.w3.org/TR/DOM-Level-2-Core/
|Status=Recommendation
|Relevant_changes=Section 1.2
}}{{Related Specification
|Name=Document Object Model (DOM) Level 1
|URL=http://www.w3.org/TR/REC-DOM-Level-1
|Status=Recommendation
|Relevant_changes=Section 1.2
}}{{Related Specification
|Name=DOM
|URL=http://dom.spec.whatwg.org/
|Status=Living Standard
|Relevant_changes=Section 6.8
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
|Note=There is an optional '''flag''' parameter that accepts one of the following values - <code>0</code> (default) - case insensitive attribute name search. 1 - case sensitive attribute name search. 2 - return the value as a string (as opposed to Boolean), however, note that what used to return as <code>true</code>, would not return as the name of the attribute, but a decimal representation of <code>true</code> in COM, which is <code>65535</code>. 4 - return the value as a fully expanded URL, which only works for URL attributes such as [[html/attributes/action|'''action''']],  [[html/attributes/background (Body element)|'''background''']],  [[html/attributes/BaseHref|'''BaseHref''']],  [[html/attributes/cite|'''cite''']],  [[html/attributes/codeBase|'''codeBase''']],  [[html/attributes/data|'''data''']],  '''dynsrc''',  [[html/attributes/href|'''href''']],  [[html/attributes/longDesc|'''longDesc''']],  [[html/attributes/lowsrc|'''lowsrc''']],  [[html/attributes/pluginspage|'''pluginspage''']],  '''profile''',  [[html/attributes/src (input, img)|'''src''']],  [[dom/properties/vrml|'''vrml''']].
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