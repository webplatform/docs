{{Page_Title|window.location.href}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The full url for this resource. Synonymous with <code>String(window.location)</code>.}}
{{API_Object_Property
|Property_applies_to=apis/location
|Read_only=Yes
|Example_object_name=window.location
|Return_value_name=
|Javascript_data_type=String
|Return_value_description=The full url for this resource.

For example, <code>http://example.org/index.html?page=1#foo</code> would return the full href of <code>http://example.org/index.html?page=1#foo</code>.
|Example_value_name=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=<code>window.location.href</code> is the same as the <code>toString</code> method of <code>window.location</code>, so you can choose to use either variable when using comparing as a string.
|Code=if(window.location == window.location.href){
    // This equates to true
    alert("These values are the same.")/
}
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=
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