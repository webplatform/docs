{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Add values, syntax, description, specifications, compatibility.
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The ‘width’ media feature describes the width of the targeted display area of the output device. For continuous media, this is the width of the viewport (as described by CSS2, section 9.1.1 [CSS21]) including the size of a rendered scroll bar (if any). For paged media, this is the width of the page box (as described by CSS2, section 13.2 [CSS21]).}}
{{CSS_Media_Feature
|Content=The width media query returns the width of the layout viewport, also called the initial containing block. This is equal to the default width of the html element. Thus, it tells you how much space the browser allows your CSS layout to take.

The width media query is one of the two vital ingredients of responsive web design; the other one is the [[tutorials/mobile_viewport|meta viewport tag]]. The width media query is very reliable across browsers, and using it will not raise compatibility issues.

The width media query is always, in all browsers, equal to document.documentElement.clientWidth.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=
|Notes=
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
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}



@media screen and (min-width: 400px) and (max-width: 700px) { … }