{{Page_Title|The &lt;p&gt; (paragraph) element}}
{{Flags
|Content=Incomplete,  Compatibility Incomplete
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name|p}}
{{Summary_Section|The '''p''' (for paragraph) element (&lt;p&gt;) represents a paragraph.}}
{{Markup_Element
|DOM_interface=dom/HTMLParagraphElement
|Content=The p element represents a paragraph. It cannot contain block-level elements (including p itself).

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
|URL=http://www.w3.org/TR/html5/the-p-element.html#the-p-element
|Status=W3C Working Draft
|Relevant_changes=the align attribute is obsolete
}}
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Unknown
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=8.0
|Note=Windows Internet Explorer 8. In IE8 Standards mode, the '''P''' element is automatically closed when a [[html/elements/table|'''TABLE''']] element is encountered. For example, <code>&lt;p&gt;&lt;table&gt;..&lt;/table&gt;&lt;/p&gt;</code> is now parsed as <code>&lt;p&gt;..&lt;/p&gt;&lt;table&gt;..&lt;/table&gt;</code>. For more information, see HTML Enhancements in Internet Explorer 8 and Defining Document Compatibility.
}}
}}
{{See_Also_Section
|Topic_clusters=Document Structure
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}