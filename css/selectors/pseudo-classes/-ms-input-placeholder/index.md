{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_Selector
|Content=
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example highlights the street and ZIP code fields with a custom style.

The placeholder text is displayed with the specified style until the field has focus, meaning that the field can be typed into. When the field has focus, it returns to the normal style of the input field and the placeholder text disappears.
|LiveURL=
|Code=
&lt;!DOCTYPE html &gt;
&lt;html&gt;
&lt;head&gt;
  &lt;title&gt;Placeholder style example&lt;/title&gt;
  &lt;style type{{=}}"text/css"&gt;
  input  /* normal style */
  {
    background-color:LightGray;
    color:Purple;
  }   
  input.address:-ms-input-placeholder /* placeholder only style */   
  {
    font-style:italic;        
    background-color:yellow;
    color:Red;
  }

  &lt;/style&gt;&lt;/head&gt;
&lt;body&gt;
  &lt;form id{{=}}"test"&gt;
    &lt;p&gt;&lt;label&gt;Enter Name: &lt;input id{{=}}"name" placeholder{{=}}"Your Name"/&gt;&lt;/label&gt;&lt;/p&gt;
    &lt;p&gt;&lt;label&gt;Enter Street: &lt;input id{{=}}"street" class{{=}}"address" 
placeholder{{=}}"Your address" /&gt;&lt;/label&gt;&lt;/p&gt;
    &lt;p&gt;&lt;label&gt;Enter a zip code: &lt;input type{{=}}"num" pattern{{=}}"(0-9){5}" 
id{{=}}"zip" class{{=}}"address" placeholder{{=}}"5 digit zip" /&gt;&lt;/label&gt;&lt;/p&gt;
    &lt;input type{{=}}"submit" /&gt;
  &lt;/form&gt;
&lt;/body&gt;
&lt;/html&gt;

}}}}
{{Notes_Section
|Notes=
===Remarks===
By default, placeholder text in input fields is light gray, but the ''':-ms-input-placeholder''' pseudo-class selector enables you to style it however you want.
|Import_Notes=
===Syntax===

selector
:-ms-input-placeholder
===Parameters===
;''selector'':A CSS simple selector.
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[http://go.microsoft.com/fwlink/p/?LinkId{{=}}238198 HTML5 Forms (Internet Explorer 10 Guide for Developers)]</code>
*<code>[http://go.microsoft.com/fwlink/p/?LinkId{{=}}233289 placeholder attribute]</code>
|Topic_clusters=Selectors, Pseudo-Classes
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}