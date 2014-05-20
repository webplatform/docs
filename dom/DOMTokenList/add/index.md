{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Adds one or more tokens to a DOMTokenList.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Data type=String
|Description=The token to add to the DOMTokenList.
|Optional=No
}}
|Method_applies_to=dom/DOMTokenList
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=//adds an item to an element's classList (a DOMTokenList)
function elAddItem(elid,itemadd) {
  var classes = document.getElementById(elid).classList;
  classes.add(itemadd);
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