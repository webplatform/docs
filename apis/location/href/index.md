{{Page_Title|window.location.href}}
{{Flags}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The full url for this resource. Synonymous with <code>String(window.location)</code>.}}
{{API_Object_Property
|Property_applies_to=apis/location
|Read_only=Yes
|Example_object_name=window.location
|Javascript_data_type=String
|Return_value_description=The full url for this resource.

For example, <code>http://example.org/index.html?page=1#foo</code> would return the full href of <code>http://example.org/index.html?page=1#foo</code>.
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
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|JavaScript}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}