{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Returns the value of the content attribute within a specified namespace.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=name
|Data type=String
|Description=The name of the desired attribute within the specified namespace.
|Optional=No
}}{{Method Parameter
|Name=namespaceURI
|Data type=String
|Description=The namespace URI that defines the desired attribute, or a null value.
|Optional=No
}}
|Method_applies_to=dom/Element
|Example_object_name=element
|Return_value_name=attributeValue
|Javascript_data_type=String
|Return_value_description=The value of the content attribute, or null if it does not exist.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=// Get the first div element in the page.
var element = document.querySelector("div");
// Continue only if the element exists.
if (element) {
 console.log("The value of the data-example attribute of the first div is " + element.getAttributeNS("html", "data-example"));
}
}}
}}
{{Notes_Section
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182717 Document Object Model (DOM) Level 3 Core Specification], Section 1.4
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
|Note=May return a number or a boolean value, if the attribute were set with [[dom/methods/setAttribute|'''setAttribute''']] and a number or boolean value, respectively (<code>element.setAttribute("wow", false)</code>).
}}
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/methods/getAttribute|getAttribute]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}