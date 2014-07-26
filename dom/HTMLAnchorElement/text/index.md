{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Final review.
|Checked_Out=No
|High-level issues=
|Content=
}}
{{Standardization_Status|W3C Last Call Working Draft}}
{{API_Name}}
{{Summary_Section|Legacy. Use [[dom/Node/textContent|anchorElement.textContent]] instead. Functions identically to [[dom/Node/textContent|Node.textContent]].}}
{{API_Object_Property
|Property_applies_to=dom/HTMLAnchorElement
|Read_only=No
|Example_object_name=anchorElement
|Return_value_name=anchorText
|Javascript_data_type=String
|Return_value_description=The text content of the element.
|Example_value_name=newAnchorText
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following script replaces every instance of the letter "a" in the text of an [[html/elements/a|'''a''']] element with instances of the letter "t", using the '''text''' property for getting and setting the text.
|Code=// Caching the a element for further use.
var anchor {{=}} document.getElementById("some-anchor");
// Getting the text of the element, replacing
// any "a" with "t" using a regular expression
// and setting the result back to the text property.
// Alternatively,
// use anchor.textContent {{=}} anchor.textContent.replace(/a/g, "t"); instead.
anchor.text {{=}} anchor.text.replace(/a/g, "t");}}
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
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}