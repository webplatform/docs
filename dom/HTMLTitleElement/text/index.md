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
{{Summary_Section|Legacy. Use [[dom/Document/title|document.title]] instead. When setting, does same as [[dom/Node/textContent|textContent]]. When getting, gets a concatenated version of all of the child text nodes of a [[html/elements/title|title]] element.}}
{{API_Object_Property
|Property_applies_to=dom/HTMLTitleElement
|Read_only=No
|Example_object_name=titleElement
|Return_value_name=titleText
|Javascript_data_type=String
|Return_value_description=A concatenation of all of the child [[dom/Text|text nodes]] of the element.
|Example_value_name=newTitleText
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following script gets the text of the title element, changes "r" to "t" and sets the text back.
|Code=// Note - this example assumes that this script runs
// after the title element is created.

// Caching the first title element in the document for further use.
var title {{=}} document.getElementsByTagName("title")[0];
// Getting the text of the element, replacing the first "r"
// with "t" and setting the result back to the text property.
// Alternatively,
// use document.title {{=}} document.title.replace("r", "t"); instead.
title.text {{=}} title.text.replace("r", "t");
}}
}}
{{Notes_Section
|Usage=Use this property to get or set the title of the document.
|Notes=When the document is the main document that is shown to the user, most of the browsers show the value of this property to the user as the title of the window or page.}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Document Object Model (DOM) Level 1
|URL=http://www.w3.org/TR/REC-DOM-Level-1/level-one-html.html#ID-77500413
|Status=W3C Recommendation
}}{{Related Specification
|Name=Document Object Model (DOM) Level 2 HTML
|URL=http://www.w3.org/TR/DOM-Level-2-HTML/html.html#ID-77500413
|Status=W3C Recommendation
}}{{Related Specification
|Name=WHATWG HTML
|URL=http://www.whatwg.org/specs/web-apps/current-work/multipage/semantics.html#dom-title-text
|Status=Living Standard
}}{{Related Specification
|Name=HTML5
|URL=http://www.w3.org/TR/html5/text-level-semantics.html#dom-a-text
|Status=W3C Last Call Working Draft
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