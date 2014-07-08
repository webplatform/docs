{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Returns a FileList of the files being dragged, if any.}}
{{API_Object_Property
|Property_applies_to=dom/DataTransfer
|Read_only=Yes
|Javascript_data_type=Object
|Return_value_description=A live FileList sequence consisting of File objects representing the files being dragged (if any).
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=//retrieve list of files being dragged
function getDragFiles(e) {
  var oData = e.dataTransfer;
  var fList = oData.files;
}
}}
}}
{{Notes_Section
|Notes=This version of the API does not expose the types of the files during the drag.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML5
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
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}