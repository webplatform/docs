{{Page_Title|The <body> element}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The <body> element represents the main content of the document.}}
{{Markup_Element
|DOM_interface=dom/HTMLBodyElement
|Content====HTML information===
{{{!}} class="wikitable"
{{!}}-
!Closing Tag
{{!}}required
{{!}}-
!CSS Display
{{!}}block
{{!}}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=This example exposes the '''body''' element in javascript.
|Code=<syntaxhighlight lang="javascript">var oBody {{=}} document.body;</syntaxhighlight>
}}{{Single Example
|Language=HTML
|Description=The "'body'" element follows the "'head'" element and is contained by the "'html'" element.
|Code=<syntaxhighlight lang="html5"><html>
<head></head>
<body></body>
</html></syntaxhighlight>
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML5
|URL=http://www.w3.org/TR/html5/the-body-element.html
|Status=W3C Working Draft
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/global.html#edef-BODY
|Status=W3C Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer / Windows
|Version=8+
|Note=The value of the 'background' attribute depends on the current document compatibility mode.
}}{{Compatibility Notes Row
|Browser=Internet Explorer / Windows
|Version=6
|Note=When you use the !DOCTYPE declaration to specify standards-compliant mode, this object no longer represents the entire surface onto which a document's contents can be rendered. The object can obtain its size from its content, or you can set its size explicitly like a div object. When the !DOCTYPE declaration does not specify standards-compliant mode, and with earlier versions of Windows Internet Explorer, the body object represents the entire surface onto which a document's contents can be rendered. The size of the body object cannot be changed and is equal to the size of the window. Margins you set on this object are rendered inside the border and scrollbars of the object.
}}
}}
{{See_Also_Section
|Topic_clusters=Document Structure
|Manual_sections====Related pages (MSDN)===
*<code>CSS Enhancements in Internet Explorer 6</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}