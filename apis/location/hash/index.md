{{Page_Title|window.location.hash}}
{{Flags}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=apis/location
|Read_only=No
|Example_object_name=window.location
|Javascript_data_type=String
|Return_value_description=Returns the fragment identifier (including hash) for the current page.

For example, <code>http://example.org/#foo</code> would return the fragment identifier of <code>#foo</code>.
|Example_value_name=#foo
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=This example shows how to first check for the availability of the window.location.hash property, and then checks to see whether the second tab in our fictional web app should be displayed.
|Code=if(typeof window.location.hash != "undefined" && window.location.hash == "#tab2"){
    // Code to display the second tab goes here.
}
}}
}}
{{Notes_Section
|Usage=This property is used to see what the fragment identifier, or "hash" is for the current page is set to.
|Notes=The window.location.hash property does not work in versions of Internet Explorer prior to version 8.

This is most often used to preserve permalinks in web applications, however the [[apis/history|history API]] may be better suited to this task if legacy browser support is not required.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=8
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}
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