{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=Editing this page produces: "Warning: More than one default form is defined for this page." ?
|Checked_Out=No
|Content=Incomplete, Compatibility Incomplete
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Controls the visible highlighting of selections of text and elements. It is possible to blind out selection completely or to allow the selection of text only.}}
{{CSS Property
|Initial value=all
|Applies to=Visible elements
|Inherited=Yes
|Media=visual
|Computed value=
|Animatable=No
|CSS object model property=
|CSS percentages=
|Values={{CSS Property Value
|Data Type=none
|Description=None of the descendants of the element can be selected, neither text nor images.
}}{{CSS Property Value
|Data Type=text
|Description=Only text of the element and its descendants can be selected.
}}{{CSS Property Value
|Data Type=all
|Description=Default. Everything, text and images, can be selected.
}}{{CSS Property Value
|Data Type=element
|Description=Only specified elements can be selected. Only supported in Firefox and Internet Explorer.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Deactivate selection of text for elements with the class '''no-select'''.
|Code=.no-select {
    user-select: none;
}
|LiveURL=http://jsfiddle.net/R5Ygm/
}}
}}
{{Notes_Section
|Usage=Needs vendor prefixes.
|Notes=Also works on mobile devices to suppress selection by touch and hold.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=User Interface for CSS3
|URL=http://www.w3.org/TR/2000/WD-css3-userint-20000216
|Status=W3C Working Draft
|Relevant_changes=
}}
}}
{{See_Also_Section
|Topic_clusters=CSS Attributes
|Manual_links=
|External_links=
|Manual_sections====Related pages (MSDN)===
*<code>[http://go.microsoft.com/fwlink/p/?LinkID{{=}}235901 IE Test Drive: User-Select]</code>
*<code>[https://developer.mozilla.org/en-US/docs/CSS/user-select]</code>
}}
{{Topics|CSS, Design}}
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
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=Basic Support
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=1
|Firefox_supported=Unknown
|Firefox_version=
|Firefox_prefixed_supported=Yes
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Yes
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Yes
}}{{Compatibility Table Desktop Row
|Feature=element
|Chrome_supported=No
|Chrome_version=
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Unknown
|Firefox_version=
|Firefox_prefixed_supported=Yes
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Yes
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Unknown
|Android_version=
|Android_prefixed_supported=Yes
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Yes
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Unknown
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Yes
}}
|Notes_rows=
}}



{{CSS_Selector
|Content=
}}