{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Sets or gets the string value of a cookie.}}
{{API_Object_Property
|Property_applies_to=dom/document
|Read_only=No
|Example_object_name=document
|Return_value_name=cookies
|Javascript_data_type=String
|Return_value_description=The current cookies of the document.
|Example_value_name=newCookie
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=A cookie is a small piece of information. Each cookie is stored in a name{{=}}value pair called a crumb—that is, if the cookie name is "id" and you want to save the id value as "this," the cookie is saved as id{{=}}this. You can store up to a maxium of 50 name{{=}}value pairs in a cookie; the cookie is always returned as a string of all the cookies that apply to the document. This means that you must parse the string returned to find the values of individual cookies.

Cookies accumulate each time the property is set. Once the maximum pair limit is reached, subsequent set will push older name{{=}}value pair off in favor of the new name{{=}}value pair.
You can use the [[concepts/programming/javascript/core_objects#String_Object|split]] method to extract a value stored in a cookie.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 2 HTML
|URL=http://www.w3.org/TR/DOM-Level-2-HTML/
|Status=Recommendation
|Relevant_changes=Section 1.5
}}{{Related Specification
|Name=WHATWG HTML
|URL=http://www.whatwg.org/specs/web-apps/current-work/multipage
|Status=Living Standard
|Relevant_changes=Section 3.1.1
}}{{Related Specification
|Name=W3C HTML5
|URL=http://www.w3.org/TR/html5/
|Status=Working Draft
|Relevant_changes=Section 3.1.1
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>Conceptual</code>
*<code>Introduction to Persistence</code>
*<code>Privacy in Internet Explorer 6</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}