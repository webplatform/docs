{{Page_Title}}
{{Flags
|State=Unreviewed
|Checked_Out=No
|High-level issues=Needs Review
|Content=Examples Needed
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Returns an array listing the formats that were set in the '''dragstart''' event. If any files are being dragged, one of the types will be the string "Files".}}
{{API_Object_Property
|Property_applies_to=dom/DataTransfer
|Read_only=Yes
|Example_object_name=event.dataTransfer
|Return_value_name=dragTypes
|Javascript_data_type=DOM Node
|Return_value_description=An array of dragged formats.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=//retrieve array of formats being dragged
function getDragTypes(e) {
  var oData = e.dataTransfer;
  var dTypes = oData.types;
}
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML
|URL=http://www.w3.org/TR/html5/editing.html
|Status=Candidate Recommendation
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
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}