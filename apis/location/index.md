{{Page_Title|window.location}}
{{Flags}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The location object provides access to the address related properties of the current document.}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Redirect the current page to example.org.
|Code=window.location = "http://example.org";
}}{{Single Example
|Description=Show an alert if the current page is example.org.
|Code=if(window.location == "http://example.org/"){
    alert("Welcome to example.org!");
}
}}
}}
{{Notes_Section
|Usage=The location object can be used as an object or a string.

Regular string comparisons such as in the examples section can be used, but there are several other properties of the location such as the hash or the hostname that can be compared individually.
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