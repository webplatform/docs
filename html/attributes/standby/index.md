{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Markup_Attribute
|Applies_to=html/elements/object
|Property_applies_to=dom/HTMLElement
|Content=A message for the browser to show while an <code>object</code>'s implementation and data load.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The <code>standby</code> attribute used to alert users to a lengthy delay before the image displays.
|Code=<object data="huge-picture.png" standby="Loading...">
</object>
}}
}}
{{Notes_Section
|Usage='''Valid up to HTML 4 only.''' Removed in HTML 5.
|Notes====Remarks===
This property has no default value.

Windows Internet Explorer does not render the '''standby''' message while loading an object's implementation or data; however, some objects may react to or display the content of this string.

'''standby''' was introduced in Microsoft Internet Explorer 6
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 2.5.5
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML5 differences from HTML4: Obsolete Attributes
|URL=http://dev.w3.org/html5/html4-differences/#obsolete-attributes
|Status=Editor's Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=2
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Unknown
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=8
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=10
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=4
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row}}
}}
{{See_Also_Section
|Topic_clusters=HTML, Multimedia
|External_links=* http://dev.w3.org/html5/html4-differences/
* http://reference.sitepoint.com/html/object/standby
|Manual_sections====Related pages (MSDN)===
*<code>object</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/HTML/Element/object]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}