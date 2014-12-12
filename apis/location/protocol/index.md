{{Page_Title|window.location.protocol}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Sets or retrieves the protocol portion of a URL.
The protocol the current document was accessed via (everything preceding the "//").
}}
{{API_Object_Property
|Property_applies_to=apis/location
|Read_only=Yes
|Example_object_name=window.location
|Return_value_name=
|Javascript_data_type=String
|Return_value_description=The protocol the current document was accessed via.

For example, <code>http://example.org/</code> would return the protocol <code>http:</code>.
|Example_value_name=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example assumes your document has a div element with id 'hostDiv', like this.
|Code=// Get the protocol from window.location
var hostpr = window.location.protocol;

// Get a div element with id 'hostDiv'
var container = document.getElementById('hostDiv');

// Fill in the div element with the host protocol
container.innerHTML = hostpr;
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
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}