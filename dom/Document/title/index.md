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
{{Summary_Section|Gets or sets the title of a [[dom/Document|Document]]. When the document is the main document that is shown (meaning, not of an [[html/elements/iframe|iframe]]), this is usually shown to the user.}}
{{API_Object_Property
|Property_applies_to=dom/Document
|Read_only=No
|Example_object_name=document
|Return_value_name=documentTitle
|Javascript_data_type=String
|Return_value_description=The current title of the document.
|Example_value_name=newDocumentTitle
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following script replaces every instance of the letter "a" in the text of an [[html/elements/a|'''a''']] element with instances of the letter "t", using the '''title''' property for getting and setting the text.
|Code=// Getting the title of the document, replacing the first "r"
// with "t" and setting the result back to the text property.
document.title {{=}} document.title.replace("r", "t");}}
}}
{{Notes_Section
|Usage=Use this property to get or set the title of the [[dom/Document|document]].
|Notes=When [[dom/Document|document]] is the main document that is shown to the user, most browsers show the value of this property to the user as the title of the window or page.}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=WHATWG HTML
|URL=http://www.whatwg.org/specs/web-apps/current-work/multipage/dom.html#document.title
|Status=Living Standard
}}{{Related Specification
|Name=HTML5
|URL=http://www.w3.org/TR/html5/dom.html#document.title
|Status=W3C Last Call Working Draft}}
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