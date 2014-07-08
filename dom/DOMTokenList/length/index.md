{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Returns the number of tokens in a DOMTokenList.}}
{{API_Object_Property
|Property_applies_to=dom/DOMTokenList
|Read_only=Yes
|Javascript_data_type=Number
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=//returns the number of classes in an element's classList (a DOMTokenList)
function elNumClasses(elid) {
  var classes = document.getElementById(elid).classList;
  return classes.length;
}
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C DOM4
|URL=http://www.w3.org/TR/dom/
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