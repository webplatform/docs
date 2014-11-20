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
|Notes====Remarks===
The default font is fixed pitch.

Firefox for Android, by default, sets a <code>[[css/properties/background-image|background-image]]</code> gradient on all '''textarea''' elements. This can be disabled using <code>background-image: none</code>.

Safari Mobile for iOS applies a default style of [[css/properties/opacity|<code>opacity</code>]]<code>: 0.4</code> to disabled [[html/elements/textarea|<code>textarea</code>]] elements. Other major browsers don't currently share this particular default style.

'''Security Warning:  '''Using this object incorrectly can compromise the security of your application. When submitting text through <code>textarea</code> over an intranet or the Internet, validating the text string is recommended. For instance, you might validate the string for a restricted set of known, good values (such as  letters and numbers) and ignore the rest.
|Import_Notes====Standards information===
*[http://www.w3.org/TR/html401/interact/forms.html#h-17.7 HTML 4.01 Specification, Section 17.7]


===HTML information===
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
|Name=HTML4 Specification
|URL=http://www.w3.org/TR/html401/cover.html
|Status=W3C Recommendation
|Relevant_changes=Section 17.7
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