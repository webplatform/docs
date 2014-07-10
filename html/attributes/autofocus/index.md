{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Provides a way to direct a user to a specific field when a document loads.}}
{{Markup_Attribute
|Applies_to=[[html/elements/input|HTMLInputElement]]
|Property_applies_to=dom/HTMLElement
|Content=This is the one of the important attribute introduced in HTML5 for UX. When used on an element, focus is set on that element on page load or when its dialog is shown (such as when a modal window is shown).

This can provide both direction and convenience for a user, reducing the need to click or tab to a field when a page opens.

This attribute is true when present on an element, and false when missing. Only one element on each page can have the autofocus field.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Code=<input id="search_box" autofocus>
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML5
|URL=http://www.w3.org/TR/html5/forms.html#attr-fe-autofocus
|Status=W3C Candidate Recommendation
}}
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
|Topic_clusters=HTML
|External_links=* [http://www.xpertdeveloper.com/2012/09/html5-autofocus/ HTML5 Autofocus Explained]
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/HTMLBGSoundElement|HTMLButtonElement]]</code>
*<code>[[dom/HTMLInputElement|HTMLInputElement]]</code>
*<code>[[dom/HTMLSelectElement|HTMLSelectElement]]</code>
*<code>[[dom/HTMLTextAreaElement|HTMLTextAreaElement]]</code>
}}
{{Topics|HTML, Usability}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}