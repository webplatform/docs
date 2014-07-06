{{Page_Title|p}}
{{Flags
|State=In Progress
|Editorial notes=Add Category, Parent and Children information. Complete Compatibility table.
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The '''p''' (for paragraph) element (&lt;p&gt;) represents a paragraph.}}
{{Markup_Element
|DOM_interface=dom/HTMLParagraphElement
|Content=p cannot contain block-level elements (including p itself).

===HTML information===
{{{!}} class="wikitable"
{{!}}-
!Closing Tag
{{!}}optional
{{!}}-
!CSS Display
{{!}}block
{{!}}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''p''' element to create a paragraph.
|Code=<syntaxhighlight lang="html5"><p>This is a paragraph.</p></syntaxhighlight>
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 4.01 Specification
|URL=http://www.w3.org/TR/html401/struct/text.html#h-9.3.1
|Status=W3C Recommendation
}}{{Related Specification
|Name=HTML5
|URL=http://www.w3.org/html/wg/drafts/html/master/grouping-content.html#the-p-element
|Status=W3C Working Draft
|Relevant_changes=The align attribute is obsolete.
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=1
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=1
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=1
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=1
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=18
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=1
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=6
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=8
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_version=1
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=1
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=8
|Note=The element is automatically closed when a [[html/elements/table|'''TABLE''']] element is encountered. For example, <code>&lt;p&gt;&lt;table&gt;..&lt;/table&gt;&lt;/p&gt;</code> is now parsed as <code>&lt;p&gt;..&lt;/p&gt;&lt;table&gt;..&lt;/table&gt;</code>.
}}{{Compatibility Notes Row
|Browser=Android Browser
|Note=When placed within a [[html/elements/div|div]] element, this element might not expand to the full width of its containing element. Setting a background (a non transparent color or any background image) using CSS fixes the issue.
}}
}}
{{See_Also_Section
|Topic_clusters=Document Structure, HTML
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/HTML/Element/p
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}