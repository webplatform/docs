{{Page_Title}}
{{Flags
|State=Unreviewed
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Uses the given element to update the drag feedback image, replacing any previously specified feedback image.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=element
|Data type=Object
|Description=An "img" element, used to set the drag data store bitmap to the element's image (at its intrinsic size). If not an "img" element, used to set the drag data store bitmap to an image generated from the given element, although the mechanism for doing so is not currently specified.
|Optional=No
}}{{Method Parameter
|Index=0
|Name=x
|Data type=unsigned long
|Description=The "x" value of the drag data store hot spot coordinate.
|Optional=No
}}{{Method Parameter
|Index=0
|Name=y
|Data type=unsigned long
|Description=The "y" value of the drag data store hot spot coordinate.
|Optional=No
}}
|Method_applies_to=dom/DataTransfer
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=//set new drag feedback image
function setDragImage(e) {
  var img = document.getElementById("dragimg");
  var oData = e.dataTransfer;
  oData.setDragImage (img, 0, 0);
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