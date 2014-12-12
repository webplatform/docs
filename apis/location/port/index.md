{{Page_Title|window.location.port}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The port number the document was accessed via.}}
{{API_Object_Property
|Property_applies_to=apis/location
|Read_only=Yes
|Example_object_name=window.location
|Return_value_name=
|Javascript_data_type=
|Return_value_description=The port number the document was accessed via.

For example, <code>http://example.org/</code> would return the default HTTP port number of <code>80</code>.
|Example_value_name=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example assumes your document has a div element with id 'hostDiv', like this.

|Code=// Get the port from window.location
var host = window.location.port;

// Get a div element with id 'hostDiv'
var container = document.getElementById('hostDiv');

// Fill in the div element with the port
container.innerHTML = port;
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