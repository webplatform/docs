{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/HTMLElement
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the '''documentElement''' property to get the [[dom/properties/innerdom/innerHTML|'''innerHTML''']] property of the entire document.
|LiveURL=
|Code=
&lt;SCRIPT&gt;
function fnGetHTML(){
   var sData {{=}} document.documentElement.innerHTML;
   oResults.value{{=}}sData;
}
&lt;/SCRIPT&gt;
&lt;TEXTAREA ID {{=}} oResults COLS {{=}} 50 ROWS {{=}} 10&gt;
&lt;/TEXTAREA&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The root node of a typical HTML document is the '''html''' object.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 1.2


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/document|document]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}