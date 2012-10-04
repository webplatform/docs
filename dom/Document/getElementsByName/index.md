{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=v|Data type=BSTR|Description=A '''String''' that specifies the value of a [[html/attributes/name|'''NAME''']] attribute.|Optional=}}
|Method_applies_to=dom/document,dom/Element
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description='''IHTMLElementCollection'''

'''NAME'''


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the '''getElementsByName''' method to return a collection of '''input type{{=}}text''' elements with the specified [[html/attributes/name|'''NAME''']] attribute value, <code>firstName</code>.
|LiveURL=
|Code=
&lt;SCRIPT&gt;
function fnGetNames(){
   // Returns a collection with 2 INPUT type{{=}}text elements.
   var aInput{{=}}document.getElementsByName("firstName");
}
&lt;/SCRIPT&gt;
&lt;INPUT TYPE{{=}}"text" NAME{{=}}"firstName"&gt;
&lt;INPUT TYPE{{=}}"text" NAME{{=}}"firstName"&gt;
&lt;INPUT TYPE{{=}}"button" VALUE{{=}}"Get Names" onclick{{=}}"fnGetNames()"&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
When you use the '''getElementsByName''' method, all elements in the document that have the specified [[html/attributes/name|'''NAME''']] attribute or [[html/attributes/id|'''ID''']] attribute value are returned.
Elements that support both the [[html/attributes/name|'''NAME''']] attribute and the [[html/attributes/id|'''ID''']] attribute are included in the collection returned by the '''getElementsByName''' method, but elements with a '''NAME''' [[dom/properties/expando|'''expando''']] are not included in the collection; therefore, this method cannot be used to retrieve custom tags by name.
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