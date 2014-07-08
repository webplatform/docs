{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Gets or sets the [[html/elements/body|body]] element of the document.}}
{{API_Object_Property
|Property_applies_to=dom/Document
|Read_only=No
|Example_object_name=document
|Return_value_name=bodyElement
|Javascript_data_type=DOM Node
|Return_value_description=The [[html/elements/body|body]] element of the document.
|Example_value_name=newBodyElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=//get the document's body content, append to it, set new content
function appendBody() {
    var bod = document.body.innerHTML;
    bod += "<nowiki><p></nowiki>That's all, folks!<nowiki></p></nowiki>";
    document.body.innerHTML = bod;
}
}}
}}
{{Notes_Section
|Usage=Use this property to get the [[html/elements/body|body]] element of the document, or to replace it with a new body element.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 2 HTML
|URL=http://www.w3.org/TR/2003/REC-DOM-Level-2-HTML-20030109
|Status=Recommendation
|Relevant_changes=Section 1.5
}}{{Related Specification
|Name=W3C HTML5
|URL=http://www.w3.org/TR/html5/
|Status=Working Draft
|Relevant_changes=Section 3.1.1
}}{{Related Specification
|Name=WHATWG HTML
|URL=http://www.whatwg.org/specs/web-apps/current-work/multipage/
|Status=Living Standard
|Relevant_changes=Section 3.1.1
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