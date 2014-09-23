{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Merge Candidate: html/attributes/type. Add note section.
|Checked_Out=No
|High-level issues=Merge Candidate
|Content=Incomplete, Compatibility Incomplete
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|An input field for entering a specific time value.}}
{{Markup_Element
|DOM_interface=dom/HTMLInputElement
|Content=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=Basic usage. Accepts no seconds.
|Code=<input type="time" value="09:00" min="09:00" max="17:00">
|LiveURL=
}}{{Single Example
|Language=HTML
|Description=Accepts seconds.
|Code=<input type="time" step="1">
|LiveURL=
}}{{Single Example
|Language=HTML
|Description=Accepts only hours.
|Code=<input type="time" step="3600">
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=On Safari Mobile for iOS, setting [[css/properties/display|<code>display</code>]]<code>: block</code> on an '''input''' of '''type="time"''' causes the text within the '''input''' to become vertically misaligned.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=23
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=No
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=No
|Android_version=
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=18
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=19
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Chrome for Android
|Version=30 or earlier
|Note=Users can't specify seconds or milliseconds.
}}{{Compatibility Notes Row
|Browser=Safari Mobile
|Note=Users can't specify seconds or milliseconds.
}}{{Compatibility Notes Row
|Browser=Firefox Mobile
|Note=Users can't specify seconds or milliseconds.
}}
}}