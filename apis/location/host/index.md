{{Page_Title|window.location.host}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The host property contains the host part of the the current document URL, (hostname:port).}}
{{API_Object_Property
|Property_applies_to=apis/location
|Read_only=Yes
|Example_object_name=window.location
|Javascript_data_type=String
|Return_value_description=The hostname and port number.

For example, <code>http://example.org:8080/</code> would return the host string of <code>example.org:8080</code>.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example assumes your document has a div element with id 'hostDiv', like this.
|Code=// Get the host from window.location
var host = window.location.host;

// Get a div element with id 'hostDiv'
var container = document.getElementById('hostDiv');

// Fill in the div element with the host
container.innerHTML = host;
|LiveURL=http://fiddle.jshell.net/YJEhh/4/
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
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