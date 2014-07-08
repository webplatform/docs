{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Gets the object that has the focus when the parent document has focus. If no element in the document has focus, returns the <code><body></code> element.}}
{{API_Object_Property
|Property_applies_to=dom/Document
|Read_only=Yes
|Example_object_name=document
|Return_value_name=element
|Javascript_data_type=DOM Node
|Return_value_description=The currently active element of the document, or <code><body></code> if no element is active.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=//display tag name of currently focused element
function getActiveElement () {
    if (document.activeElement) {
        alert(document.activeElement.tagName);
    }
}
}}
}}
{{Notes_Section
|Notes=The active element retains focus in the parent [[dom/Document|'''Document''']] even when focus is shifted from the parent to another application. If the focus returns to the parent '''document''', focus also returns to the same active element.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=WHATWG HTML
|URL=http://www.whatwg.org/specs/web-apps/current-work/multipage
|Status=Living Standard
|Relevant_changes=Section 3.1.1
}}{{Related Specification
|Name=W3C HTML5
|URL=http://www.w3.org/TR/html5/editing.html
|Status=Candidate Recommendation
|Relevant_changes=Section 7.4.3
}}{{Related Specification
|Name=W3C HTML5
|URL=http://www.w3.org/TR/html5/dom.html
|Status=Candidate Recommendation
|Relevant_changes=Section 3.1.1
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Note=You can set the active element with the [[dom/HTMLElement/setActive|'''setActive''']] method or the [[dom/HTMLElement/focus|'''focus''']] method; however, using the '''setActive''' method has no effect on document focus. Use the '''focus''' method to cause an individual element to gain focus and become the active element.
}}{{Compatibility Notes Row
|Browser=Internet Explorer
|Version=4
|Note=Returns [[html/elements/body]] when it is accessed inline during the loading of a document.
}}{{Compatibility Notes Row
|Browser=Internet Explorer
|Version=5 and later
|Note=This property is not defined until a document is loaded. A value of null is given for this property, if it is accessed inline during the loading of a document. This property can be accessed in the [[dom/Element/load|'''onload''']] event handler function.
}}
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