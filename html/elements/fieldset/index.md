{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The '''fieldset''' element is used to group related elements in a form.

}}
{{Markup_Element
|DOM_interface=dom/HTMLFieldSetElement
|Content=Typically, the browser draws a box around the text and other elements that the field set contains.

===Attributes (HTML 5)===

; disabled : If this Boolean attribute is set, the form controls that are its descendants, except descendants of its first optional '''legend''' element, are disabled, i.e., not editable. They won't receive any browsing events, like mouse clicks or focus-related ones. Often browsers display such controls as gray.

; form : This attribute has the value of the id attribute of the '''form''' element its related to. Its default value is the id of the nearest <form> element it is a descendant of.

; name : The name associated with the group, which is submitted with the form data. ''The label for the field set is given by the first '''legend''' element that is a child of this field set.''




}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
This element is useful for grouping elements in a form and for distinctively marking text in a document.
The '''FIELDSET''' element has the same behavior as a window frame. Because window frames do not have scroll bars, assigning the [[css/properties/overflow|'''overflow''']] property a value of '''scroll''' will render it as if the value were '''hidden'''.
Build date: 7/24/2012
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML5
|URL=http://www.w3.org/TR/html5/forms.html#the-fieldset-element
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
{{See_Also_Section
|Topic_clusters=HTML
|Manual_links=* [[html/elements/legend|'''legend''']] element
* [[html/elements/form|'''form''']] element
|External_links=* http://www.w3.org/TR/html5/forms.html#the-fieldset-element
* http://www.w3.org/TR/html-markup/fieldset.html#fieldset
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/Web/HTML/Element/fieldset
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}