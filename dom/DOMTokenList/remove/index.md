{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Removes one or more tokens from a DOMTokenList.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=token
|Data type=String
|Description=The token to remove from the DOMTokenList.
|Optional=No
}}
|Method_applies_to=dom/DOMTokenList
|Javascript_data_type=Boolean
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=//removes an item from an element's classList (a DOMTokenList)
function elRemItem(elid,itemrem) {
  var classes = document.getElementById(elid).classList;
  classes.remove(itemrem);
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