{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Just a final review is probably needed.
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Gets the content of a <code><textarea></code> element.}}
{{API_Object_Property
|Property_applies_to=dom/HTMLTextAreaElement
|Read_only=No
|Example_object_name=textAreaElement
|Return_value_name=textAreaContent
|Javascript_data_type=String
|Return_value_description=The content of the element, whether entered, existing or otherwise visible.
|Example_value_name=newTextAreaContent
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following code uses this property to log the content of a <code><textarea></code> and its length.
|Code=// Declaring the used variables first.
var textAreaList, textArea;

// Getting any <textarea> in the page
textAreaList = document.getElementsByTagName("textarea");

// Verifying there is at least one.
if (textAreaList.length) {

    // Getting the first <textarea> in the page.
    textArea = textAreaList[0];

   // Logging the content of the first <textarea> in the page.
    console.log("The content of the first textarea element is - " +
        textArea.value);

    // Logging the codepoint length of the
    // content of the first <textarea> in the page.
    console.log("The codepoint length of the content of the first textarea element is - " +
        textArea.value.length);
}
|LiveURL=
}}
}}
{{Notes_Section
|Usage=Use this property to get the content of <textarea>.
|Notes=In JavaScript/ECMAScript, the [[javascript/String/length|length]] property of this property can be used to determine the codepoint length of the content.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Document Object Model (DOM) Level 1
|URL=http://www.w3.org/TR/REC-DOM-Level-1/level-one-html.html#ID-70715579
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related Specification
|Name=Document Object Model (DOM) Level 2 HTML
|URL=http://www.w3.org/TR/DOM-Level-2-HTML/html.html#ID-70715579
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related Specification
|Name=W3C HTML5
|URL=http://www.w3.org/TR/html/forms.html#dom-textarea-value
|Status=W3C Candidate Recommendation
|Relevant_changes=
}}{{Related Specification
|Name=WHATWG HTML
|URL=http://www.whatwg.org/specs/web-apps/current-work/multipage/forms.html#dom-textarea-value
|Status=Living Standard
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}