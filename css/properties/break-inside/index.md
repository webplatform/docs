{{Page_Title|break-inside}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Control page/column/region breaks that fall within a block of content}}
{{CSS Property
|Initial value=auto
|Applies to=block-level elements
|Inherited=No
|Media=visual
|Animatable=No
|CSS object model property=breakInside
|Values={{CSS Property Value
|Data Type=auto
|Description=Default. A page/column/region break is determined  by the flow of content.
}}{{CSS Property Value
|Data Type=avoid
|Description=A page/column/region break is not allowed within the content block.
}}{{CSS Property Value
|Data Type=avoid-page
|Description=A page break is not allowed within the content block.
}}{{CSS Property Value
|Data Type=avoid-column
|Description=A column break is not allowed within the content block.
}}{{CSS Property Value
|Data Type=avoid-region
|Description=A [[css/concepts/region|region]] break is not allowed within the content block.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/* forces top-level headings onto a new page, column, or region */
h1 {
    break-before: always;
}

/* binds subheads to subsequent content,
   without necessarily forcing a page break */
h2, h3 {
    break-after: avoid;
    break-inside: avoid;
}
}}
}}
{{Notes_Section
|Usage=This property replaces separate '''column-break-inside''', '''page-break-inside''', and '''region-break-inside''' properties, which may still be present in some browser implementations.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Regions Module Level 3
|URL=http://dev.w3.org/csswg/css3-regions/
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=No
|Chrome_version=
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=11.1
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=Support for non standard column-break-inside
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Yes
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
|Safari_prefixed_supported=Yes
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Multi-Column, Regions
|External_links=* W3C editor's draft: [http://dev.w3.org/csswg/css3-regions/ CSS Regions Module Level 3]
* Adobe Web Standards: [http://html.adobe.com/webstandards/cssregions CSS Regions]
* Adobe Developer's Network: [http://www.adobe.com/devnet/html5/articles/css3-regions.html CSS3 Regions: Rich page layout with HTML and CSS3]
* [http://adobe.github.com/web-platform/samples/css-regions Sample pages]
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]&amp;lt;/code>
*<code>[[css/cssom/currentStyle|currentStyle]]&amp;lt;/code>
*<code>[[css/cssom/style|style]]&amp;lt;/code>
*<code>address&amp;lt;/code>
*<code>blockQuote&amp;lt;/code>
*<code>div&amp;lt;/code>
*<code>dl&amp;lt;/code>
*<code>fieldSet&amp;lt;/code>
*<code>form&amp;lt;/code>
*<code>noFrames&amp;lt;/code>
*<code>noScript&amp;lt;/code>
*<code>ol&amp;lt;/code>
*<code>p&amp;lt;/code>
*<code>pre&amp;lt;/code>
*<code>[[html/elements/table|table]]</code>
*<code>ul</code>
*<code>dd</code>
*<code>dt</code>
*<code>li</code>
*<code>tBody</code>
*<code>td</code>
*<code>tFoot</code>
*<code>th</code>
*<code>tHead</code>
*<code>tr</code>
*<code>button</code>
*<code>del</code>
*<code>ins</code>
*<code>map</code>
*<code>object</code>
*<code>script</code>
*<code>Reference</code>
*<code>[[css/properties/break-after|breakAfter]]</code>
*<code>[[css/properties/break-before|breakBefore]]</code>
}}
{{Topics|CSS, CSS-Regions}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}