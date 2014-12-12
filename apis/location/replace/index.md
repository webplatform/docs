{{Page_Title|window.location.replace}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Similar to <code>[[apis/location/assign|window.location.assign]]</code>, except that it "replaces" the current document, removing the previous one from the back button history.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=url
|Data type=String
|Description=The new URL to navigate to.
|Optional=No
}}
|Method_applies_to=apis/location
|Example_object_name=window.location
|Return_value_name=
|Javascript_data_type=
|Return_value_description=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=//force a new page to load and replace the current one
window.location.replace("http://www.example.com");

|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=It is generally advisable to use <code>[[apis/location/assign|window.location.assign]]</code> becuse it retains the back button history. The <code>replace</code> method removes the current page from the back history, and therefore may confuse the user.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Window Object 1.0
|URL=http://www.w3.org/TR/Window/
|Status=W3C Working Draft
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|JavaScript}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}