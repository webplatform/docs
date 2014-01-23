{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Gets the URL of the location that referred the user to the current document.}}
{{API_Object_Property
|Property_applies_to=dom/Document
|Read_only=Yes
|Example_object_name=document
|Return_value_name=referrerURL
|Javascript_data_type=String
|Return_value_description=The URL of the referring document, or an empty string.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=*It returns a value only when the user reaches the current document through a link from the previous document. Otherwise, it returns an empty string.
For example, if DocumentA.htm includes a link to DocumentB.htm, and the user clicks that link, the <code>document</code>.'''referrer''' on DocumentB.htm returns "DocumentA.htm." However, if the user is on DocumentA.htm and types DocumentB.htm into the address line or using some kind of "Open" method of the browser to get to DocumentB.htm, it returns the empty string.
*It also returns an empty string when the link is from a secure site.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 2 HTML
|URL=http://www.w3.org/TR/2003/REC-DOM-Level-2-HTML-20030109/
|Status=Recommendation
|Relevant_changes=Section 1.5
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
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