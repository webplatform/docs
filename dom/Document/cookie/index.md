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
|Examples=}}
{{Notes_Section
|Notes=
===Remarks===
A cookie is a small piece of information. Each cookie is stored in a name{{=}}value pair called a crumb—that is, if the cookie name is "id" and you want to save the id value as "this," the cookie is saved as id{{=}}this. You can store up to a maxium of 50 name{{=}}value pairs in a cookie; the cookie is always returned as a string of all the cookies that apply to the document. This means that you must parse the string returned to find the values of individual cookies.
Cookies accumulate each time the property is set. Once the maxium pair limit is reached, subsequent set will push older name{{=}}value pair off in favor of the new name{{=}}value pair.
You can use the Microsoft JScript split method to extract a value stored in a cookie.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 2.4


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/document|document]]</code>
*<code>Conceptual</code>
*<code>Introduction to Persistence</code>
*<code>Privacy in Internet Explorer 6</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}