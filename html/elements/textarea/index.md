{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=Should have automatic child links generated.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The <code>textarea</code> tag defines a multi-line text input control.

A text area can hold an unlimited number of characters, and the text renders in a fixed-width font (usually Courier).
}}
{{Markup_Element
|DOM_interface=dom/HTMLTextAreaElement
|Content=Internationalization topics related to the <code>a</code> element:
* [http://localhost/International/techniques/authoring-html#blocks  Setting direction on block elements]
* [http://localhost/International/techniques/authoring-html#formdir Managing text direction in form controls]
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the <code>textarea</code> element to set the cascading style sheets (CSS) [[css/properties/overflow|'''overflow''']] attribute to <code>hidden</code> to remove the scroll bars from the <code>textarea</code>.
|Code=&lt;textarea style{{=}}"overflow:hidden" id{{=}}"txtComments"&gt;
   The patient is in stable condition after suffering an attack of 
   the insatiable munchies.
&lt;/textarea&gt;
|LiveURL=
}}
}}
{{Notes_Section
|Usage=To cater for international users see: [http://www.w3.org/International/techniques/authoring-html#form-dir Managing text direction in form controls]

== HTML Attributes ==
; Global attributes<nowiki>:</nowiki> accesskey, class, contenteditable, dir, hidden, id, lang, spellcheck, style, tabindex, title, translate
: See [[html/global attributes|global attributes]].

; <code>autofocus</code> = boolean
: Allows the author to indicate that a control is to be focused as soon as the page is loaded

; <code>cols</code> = non-negative integer
: specifies the expected maximum number of characters per line. by default, it is 20.

; <code>disabled</code> = boolean
: If present, make the control non-interactive and to prevent its value from being submitted.

; <code>form</code> = the ID of a form element in the element's owner
: Associate the textarea element with its form owner.<br />By default, the textarea element is associated with its nearest ancestor form element.

; <code>name</code> = unique name
: Represents the element's name.

; <code>placeholder</code> = sample value or a brief description of the expected format
: Represents a hint (a word or short phrase) intended to aid the user with data entry.<br />The placeholder attribute should not be used as an alternative to a label.

; <code>readonly</code> = boolean
: Control whether the text can be edited by the user or not.

; <code>required</code> = boolean
: When specified, the user will be required to enter a value before submitting the form.

; <code>rows</code> = valid non-negative integer
: Specifies the number of lines to show. by defult, it is 2.

; <code>wrap</code> = "soft"/ "hard":
:;soft
::The Soft state indicates that the text in the textarea is not to be wrapped when it is submitted (though it can still be wrapped in the rendering).
:;hard
::The Hard state indicates that the text in the textarea is to have newlines added by the user agent so that the text is wrapped when it is submitted.<br />If the element's wrap attribute is in the Hard state, the cols attribute must be specified.
|Notes====Remarks===
The default font is fixed pitch.

Firefox for Android, by default, sets a <code>[[css/properties/background-image|background-image]]</code> gradient on all '''textarea''' elements. This can be disabled using <code>background-image: none</code>.

Safari Mobile for iOS applies a default style of [[css/properties/opacity|<code>opacity</code>]]<code>: 0.4</code> to disabled [[html/elements/textarea|<code>textarea</code>]] elements. Other major browsers don't currently share this particular default style.

'''Security Warning:  '''Using this object incorrectly can compromise the security of your application. When submitting text through <code>textarea</code> over an intranet or the Internet, validating the text string is recommended. For instance, you might validate the string for a restricted set of known, good values (such as  letters and numbers) and ignore the rest.
|Import_Notes====HTML information===
{{{!}} class="wikitable"
{{!}}-
!Closing Tag
{{!}}required
{{!}}-
!CSS Display
{{!}}inline
{{!}}}


 
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/forms.html#the-textarea-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/forms.html#the-textarea-element
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/interact/forms.html#edef-TEXTAREA
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