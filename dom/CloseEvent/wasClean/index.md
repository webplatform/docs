{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs spec reference, standardization status
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Indicates whether the server connection closed cleanly.}}
{{API_Object_Property
|Property_applies_to=dom/CloseEvent
|Read_only=Yes
|Example_object_name=event
|Return_value_name=wasClean
|Javascript_data_type=Boolean
|Return_value_description=Whether the connection was cleanly closed.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=function getCloseClean(e) {
//retrieve whether connection was cleanly closed 
var closeClean = e.wasClean;
return closeClean;
}
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
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}