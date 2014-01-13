{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Gets a list of elements with a specified name attribute value.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=name
|Data type=String
|Description=The value of a [[html/attributes/name|'''NAME''']] attribute.
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
|Description=This example uses the '''getElementsByName''' method to return a collection of '''input type{{=}}text''' elements with the specified [[html/attributes/name|'''NAME''']] attribute value, <code>firstName</code>.
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
|Name=DOM Level 3 Core
|URL=http://www.w3.org/TR/DOM-Level-3-Core/
|Status=Recommendation
|Relevant_changes=Section 1.4
}}
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Note=When you use the '''getElementsByName''' method, all elements in the document that have the specified [[html/attributes/name|'''NAME''']] attribute or [[html/attributes/id|'''ID''']] attribute value are returned. Elements that support both the [[html/attributes/name|'''NAME''']] attribute and the [[html/attributes/id|'''ID''']] attribute are included in the collection returned by the '''getElementsByName''' method, but elements with a '''NAME''' [[dom/properties/expando|'''expando''']] are not included in the collection; therefore, this method cannot be used to retrieve custom tags by name.
}}
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/Document|Document]]</code>
*<code>About the W3C Document Object Model</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}