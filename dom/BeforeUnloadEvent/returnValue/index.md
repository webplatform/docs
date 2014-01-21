{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Gets or sets a value that indicates whether to warn the user prior to navigating away from a page.}}
{{API_Object_Property
|Property_applies_to=dom/BeforeUnloadEvent
|Read_only=No
|Example_object_name=event
|Return_value_name=returnValue
|Javascript_data_type=String
|Return_value_description=The text that will be shown to the user.
|Example_value_name=preventNavigationReason
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=The [[dom/BeforeUnloadEvent|'''BeforeUnloadEvent''']] allows you to warn a user who is navigating away from a page or closing the browser. Set the return value to false or a string value to cancel the document unload event. You can also return a string or '''Boolean''' value from the event handler to display a message to the user, who is asked to confirm that they want to unload the document.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML5
|URL=http://www.w3.org/TR/html5/
|Status=Working Draft
|Relevant_changes=Section 5.10.10
}}{{Related Specification
|Name=WHATWG HTML
|URL=http://www.whatwg.org/specs/web-apps/current-work/multipage
|Status=Living Standard
|Relevant_changes=Section 5.10.10
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=9 and later
|Note=The warning dialog box is easier to read  than in earlier versions.  In the improved dialog box, it is easier to distinguish the default text from text provided by the website, and large buttons clearly indicate how to stay on the page or navigate away.
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