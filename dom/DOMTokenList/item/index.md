{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs compat table
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Returns a specific zero-indexed token from a DOMTokenList.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=index
|Data type=Number
|Description=The index of the token to retrieve.
|Optional=No
}}
|Method_applies_to=dom/DOMTokenList
|Javascript_data_type=String
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=//returns a specific item from an element's classList (a DOMTokenList)
function elItem(elid,num) {
  var classes = document.getElementById(elid).classList;
  return classes.item(num);
}
}}
}}
{{Notes_Section
|Usage=<code>DOMTokenList.item(n)</code> is functionally equivalent to <code>DOMTokenList[n]</code> in that it references an indexed item in the DOMTokenList.
}}
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