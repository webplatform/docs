{{Page_Title}}
{{Flags
|High-level issues=Unreviewed Import
|Content=Compatibility Incomplete
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Provides a way to direct a user to a specific field when a document loads. This can provide both direction and convenience for a user, reducing the need to click or tab to a field when a page opens. This attribute is true when present on an element, and false when missing.}}
{{Markup_Attribute
|Applies_to=[[html/elements/input|HTMLInputElement]]
|Property_applies_to=dom/HTMLElement
|Content=This is the one of the important attribute introduced in HTML5 in terms of UX. With this attribute we can focus required element without any JavaScript code. And all you need to do is place one attribute to HTML element.

For example if we look at Facebook home page you can see that cursor is automatically pointed to email id field which makes user to just type in the credentials.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Code=<input id="search_box" autofocus>
}}
}}
{{Notes_Section
|Notes====Remarks===
Only one control in a document can have autofocus specified. If more than one element has the attribute, only the first one in the page will get the focus when the page opens. This is a boolean attribute, requiring only the presence of the attribute to be true.
The following example shows a field that will receive focus when a page opens.
'''Note'''  For more  code samples, see [http://go.microsoft.com/fwlink/p/?LinkID{{=}}251128 Form controls part 1] and [http://go.microsoft.com/fwlink/p/?LinkID{{=}}251131 Form controls part 2: validation] on the Windows Internet Explorer sample site.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 4.10.19.4
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=6+
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=4+
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=11+
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5+
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|External_links=* [http://www.xpertdeveloper.com/2012/09/html5-autofocus/ HTML5 Autofocus Explained]
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/HTMLBGSoundElement|HTMLButtonElement]]</code>
*<code>[[dom/HTMLInputElement|HTMLInputElement]]</code>
*<code>[[dom/HTMLSelectElement|HTMLSelectElement]]</code>
*<code>[[dom/HTMLTextAreaElement|HTMLTextAreaElement]]</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}