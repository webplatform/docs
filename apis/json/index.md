{{Page_Title}}
{{Flags
|High-level issues=Stub
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|JSON is a native API for parsing and serialising information to the JSON format.

JSON contains two methods: <code>parse</code> for parsing JSON strings, and <code>stringify</code> for converting a JavaScript object into JSON.
}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Convert a JavaScript object to a string.
|Code=var js_object = {
    type: "This is a Javascript Object."
};

var json_string = JSON.stringify(js_object);

}}{{Single Example
|Language=JavaScript
|Description=Parse a JSON string to a JavaScript object.
|Code=var json_string = '{type:"This is a JSON Object."}';
var js_object = JSON.parse(json_string);
alert(js_object.type);
}}
}}
{{Notes_Section
|Notes=This object can also be polyfilled for older browsers that don't support it.
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
|Internet_explorer_version=7
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