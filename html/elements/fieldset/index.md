{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The '''fieldset''' element is used to group related elements in a form.}}
{{Markup_Element
|DOM_interface=dom/HTMLFieldSetElement
|Content=The fieldset element represents a set of form controls. Optionally grouped under a common name with an additional '''legend''' element.

HTML5 adds the following attributes which are fully optional.

===Attributes (HTML 5)===

; disabled : If this Boolean attribute is set, the form controls that are its descendants, except descendants of its first optional '''legend''' element, are disabled, i.e., not editable. They won't receive any browsing events, like mouse clicks or focus-related ones. Often browsers display such controls as gray.

; form : This attribute has the value of the id attribute of the '''form''' element its related to. Its default value is the id of the nearest <form> element it is a descendant of.

; name : The name associated with the group, which is submitted with the form data. ''The label for the field set is given by the first '''legend''' element that is a child of this field set.''
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=Simple form with fieldset, legend, and label elements.
|Code=<form action="" method="post">
  <fieldset>
    <legend>Title</legend>
    <label for="radio">Click me</label>
    <input type="radio" name="radio" id="radio">
  </fieldset>
</form>
|LiveURL=http://code.webplatform.org/gist/f77f0a06304503ecddd6
}}
}}
{{Notes_Section
|Usage=Fieldsets are not required but useful for grouping elements in a form to enhance the visual flow and usability of complex forms. optionally you can use a [[html/elements/legend]'''legend'''] element to give your '''fieldset''' element a caption.
|Notes====Default layout===
Typically, the browser draws a box around the containing elements of every fieldset. This border can be disabled via CSS <code>border: none;</code> The border contains the legend by default. See [[html/elements/legend]'''legend'''] for details.

===Nesting fieldsets===

}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML5
|URL=http://www.w3.org/TR/html5/forms.html#the-fieldset-element
|Status=W3C Candidate Recommendation
}}{{Related Specification
|Name=HTML 4.01 Specification
|URL=http://www.w3.org/TR/html401/
|Status=W3C Recommendation
|Relevant_changes=New attributes: disabled, form, name
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