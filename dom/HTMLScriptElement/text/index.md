{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Final review.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|W3C Last Call Working Draft}}
{{API_Name}}
{{Summary_Section|Legacy. Use [[dom/Node/textContent|textContent]] instead. When setting, does same as [[dom/Node/textContent|textContent]]. When getting, gets a concatenated version of all of the child text nodes of a [[html/elements/script|script]] element.}}
{{API_Object_Property
|Property_applies_to=dom/HTMLScriptElement
|Read_only=No
|Example_object_name=scriptElement
|Return_value_name=scriptCode
|Javascript_data_type=String
|Return_value_description=A concatenation of all of the child [[dom/Text|text nodes]] of the element.
|Example_value_name=newScriptCode
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following script gets the code of an inline script element, changes the name of a function, constructs a new scripts element, sets the changed code as its code and appends it to the document in order to run it.
|Code=// Caching the script element with the some-script ID.
var script = document.getElementById("some-script");

// Getting the script code.
// Alternatively, use script.textContent.
var scriptCode = script.text;

// Replacing the first occurrence of "function someFunction()"
// with "function newFunction()".
scriptCode = scriptCode.replace("function someFunction()", "function newFunction()");

// Creating a new script element.
var newScript = document.createElement("script");

// Setting the changed script code as its text.
// Alternatively, use newScript.textContent.
newScript.text = scriptCode;

// Appending the script element to the head element
// in order to run it.
document.head.appendChild(newScript);
}}
}}
{{Notes_Section
|Usage=Legacy. Use [[dom/Node/textContent|textContent]] instead.

Use this property to get a concatenated version of all of the child text nodes of a [[html/elements/script|script]] element.
Setting this property works the same way as setting the [[dom/Node/textContent|textContent]] property.
|Notes=* [[dom/Text|Text nodes]] that are nested within elements or HTML comments is excluded.
* Settings this property of a [[html/elements/script|'''script''']] element after its contained or referenced script has already ran does not run the new set code.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Document Object Model (DOM) Level 1
|URL=http://www.w3.org/TR/REC-DOM-Level-1/level-one-html.html#ID-46872999
|Status=W3C Recommendation
}}{{Related Specification
|Name=WHATWG HTML
|URL=http://www.whatwg.org/specs/web-apps/current-work/multipage/scripting.html#dom-script-text
|Status=Living Standard
}}{{Related Specification
|Name=HTML5
|URL=http://www.w3.org/TR/html5/scripting-1.html#dom-script-text
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
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}