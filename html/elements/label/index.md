{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Specifies a label for another element on the page.}}
{{Markup_Element
|DOM_interface=dom/HTMLLabelElement
|Tag_omissions=Closing tag required
|CSS_display=inline
|Content=The content of the label provides the caption for the input. The input can be specified in one of two ways:

# The input can be identified by the "for" attribute
# The input can be a child element of the label

User agents will often focus the cursor on the input element after clicking the associated label.

== HTML Attributes ==

; <code>form</code> = string: Associate the fieldset element with its form owner.
; <code>for</code> = string: Specified to indicate a form control with which the caption is to be associated.<br />The attribute's value must be the ID of a labelable form-associated element in the same Document as the label element.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''LABEL''' element and the [[html/attributes/accessKey|'''ACCESSKEY''']] attribute to set focus on a text box.
|Code=&lt;label for{{=}}"oCtrlID" accesskey{{=}}"1"&gt;
    #&lt;span style{{=}}"text-decoration:underline;"&gt;1&lt;/span&gt;: Press Alt+1 to set focus to textbox
&lt;/label&gt;
&lt;input type{{=}}"text" name{{=}}"txt1" value{{=}}"binding sample 1" 
       size{{=}}"20" tabindex{{=}}"1" id{{=}}"oCtrlID"/&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/accesskey.htm
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
To bind a '''LABEL''' to another control, set the [[html/attributes/dom/for|'''FOR''']] attribute of the '''LABEL''' element equal to the [[html/attributes/id|'''ID''']] of the control. Binding a '''LABEL''' to the [[html/attributes/name|'''NAME''']] attribute of the control has no effect. However, to submit a form, you must specify a '''NAME''' on the control to which the '''LABEL''' element is being bound.
There are two ways to underline the designated access key. The rich text support in the '''LABEL''' element makes it possible to wrap the '''U''' element around the character in the label text specified by the [[html/attributes/accessKey|'''ACCESSKEY''']] attribute. If you prefer to use cascading style sheets (CSS) to apply style formatting, enclose the designated character in a '''SPAN''' and set the style to <code>"text-decoration: underline"</code>.
If the user clicks the '''LABEL''', the [[dom/events/click|'''onclick''']] event fires on the '''LABEL''' and then on the control specified by the [[html/attributes/dom/for|'''htmlFor''']] property. Pressing the access key for the '''LABEL''' sets the focus but does not fire the '''onclick''' event.
Labels cannot be nested.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/forms.html#the-label-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/forms.html#the-label-element
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/interact/forms.html#edef-LABEL
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}