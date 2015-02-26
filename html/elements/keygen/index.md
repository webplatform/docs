{{Page_Title}}
{{Flags
|State=Unreviewed
|Editorial notes=
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Represents a key pair generator control}}
{{Markup_Element
|DOM_interface=dom/HTMLKeygenElement
|Tag_omissions=
|CSS_display=
|Content=When the control's form is submitted, the private key is stored in the local keystore, and the public key is packaged and sent to the server.


== HTML Attributes ==

*<code>autofocus</code> = boolean<br />Allows the author to indicate that a control is to be focused as soon as the page is loaded
*<code>challenge</code> = string<br />A challenge string that is submitted along with the public key. [[#Example_A|[Example A]]]
*<code>disabled</code> = boolean<br />If present, make the control non-interactive and to prevent its value from being submitted.
*<code>form</code> = the ID of a form element in the element's owner<br />Associate the keygen element with its form owner.<br />By default, the keygen element is associated with its nearest ancestor form element.
*<code>keytype</code> = rsa<br />The type of key generated.
*<code>name</code> = unique name<br />Represents the element's name.

}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=
|Code=<nowiki>
<keygen name="key" challenge="235ldahlae983dadfar"/>
</nowiki>
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/forms.html#the-keygen-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/forms.html#the-keygen-element
|Status=W3C Recommendation
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