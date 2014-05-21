{{Page_Title}}
{{Flags
|State=Unreviewed
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Returns a DataTransferItemList object containing the drag data.}}
{{API_Object_Property
|Property_applies_to=dom/DataTransfer
|Read_only=Yes
|Javascript_data_type=Object
|Return_value_description=A DataTransferItemList object; see the [http://www.w3.org/TR/html5/editing.html#datatransferitemlist|W3C specification] for more information.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=//get DataTransfer item list
function getItemList(e) {
  var oData = e.dataTransfer;
  var iList = oData.items;
}
}}
}}
{{Notes_Section}}
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