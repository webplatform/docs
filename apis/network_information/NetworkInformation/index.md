{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Trying to determine if this API is defined anywhere outside of the Network Information API [http://www.w3.org/TR/netinfo-api/] or if it should even be included right now. 
|Checked_Out=No
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Is exposed on the Navigator object, and all instances of the Navigator type are defined to also implement the NetworkInformation interface.}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=function show() {
  console.log(navigator.connection.bandwidth);
}

navigator.connection.addEventListener('change', show, false);

show();
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=The Network Information API
|URL=http://www.w3.org/TR/netinfo-api/
|Status=W3C Note
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|API, Mobile, Network Information}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}