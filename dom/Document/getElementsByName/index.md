{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs compat tables
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Returns ah HTMLCollection of elements in the document that have a <code>name</code> attribute with the specified value.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=name
|Data type=String
|Description=The value of a [[html/attributes/name|'''name''']] attribute.
|Optional=No
}}
|Method_applies_to=dom/Document
|Example_object_name=document
|Return_value_name=elementList
|Javascript_data_type=DOM Node
|Return_value_description=A list of elements with the a name attribute that matches the specified value.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''getElementsByName''' method to return a collection of '''input type{{=}}text''' elements with the specified [[html/attributes/name|'''name''']] attribute value, <code>firstName</code>.
|Code=&lt;script&gt;
function getFirstNames() {
   // Prints a collection with 2 input type{{=}}text elements.
   console.log(document.getElementsByName("firstName"));
}
&lt;/script&gt;
&lt;input type{{=}}"text" name{{=}}"firstName"/&gt;
&lt;input type{{=}}"text" name{{=}}"firstName"/&gt;
&lt;input type{{=}}"button" value{{=}}"Get Names" onclick{{=}}"getFirstNames()"&gt;
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 2 HTML
|URL=http://www.w3.org/TR/DOM-Level-2-HTML/html.html#ID-71555259
|Status=Recommendation
|Relevant_changes=Section 1.4
}}{{Related Specification
|Name=W3C HTML5
|URL=http://www.w3.org/html/wg/drafts/html/master/single-page.html
|Status=Editor's Draft
|Relevant_changes=Section 3.1.3
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Note=When you use the '''getElementsByName''' method, all elements in the document that have the specified [[html/attributes/name|'''NAME''']] attribute or [[html/attributes/id|'''ID''']] attribute value are returned. Elements that support both the [[html/attributes/name|'''NAME''']] attribute and the [[html/attributes/id|'''ID''']] attribute are included in the collection returned by the '''getElementsByName''' method, but elements with a '''NAME''' are not included in the collection; therefore, this method cannot be used to retrieve custom tags by name.
}}
}}
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}