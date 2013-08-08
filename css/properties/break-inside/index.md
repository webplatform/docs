{{Page_Title|break-inside}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS Property
|Initial value=auto
|Applies to=block-level elements
|Inherited=No
|Media=paged
|Animatable=No
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
|Import_Notes====Syntax===
&amp;lt;code>'''break-inside: '''auto '''{{!}}''' avoid '''{{!}}''' avoid-page '''{{!}}''' avoid-column&amp;lt;/code>
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
*&amp;lt;code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]&amp;lt;/code>
*&amp;lt;code>[[css/cssom/currentStyle|currentStyle]]&amp;lt;/code>
*&amp;lt;code>[[css/cssom/style|style]]&amp;lt;/code>
*&amp;lt;code>address&amp;lt;/code>
*&amp;lt;code>blockQuote&amp;lt;/code>
*&amp;lt;code>div&amp;lt;/code>
*&amp;lt;code>dl&amp;lt;/code>
*&amp;lt;code>fieldSet&amp;lt;/code>
*&amp;lt;code>form&amp;lt;/code>
*&amp;lt;code>noFrames&amp;lt;/code>
*&amp;lt;code>noScript&amp;lt;/code>
*&amp;lt;code>ol&amp;lt;/code>
*&amp;lt;code>p&amp;lt;/code>
*&amp;lt;code>pre&amp;lt;/code>
*&amp;lt;code>[[html/elements/table|table]]&amp;lt;/code>
*&amp;lt;code>ul&amp;lt;/code>
*&amp;lt;code>dd&amp;lt;/code>
*&amp;lt;code>dt&amp;lt;/code>
*&amp;lt;code>li&amp;lt;/code>
*&amp;lt;code>tBody&amp;lt;/code>
*&amp;lt;code>td&amp;lt;/code>
*&amp;lt;code>tFoot&amp;lt;/code>
*&amp;lt;code>th&amp;lt;/code>
*&amp;lt;code>tHead&amp;lt;/code>
*&amp;lt;code>tr&amp;lt;/code>
*&amp;lt;code>button&amp;lt;/code>
*&amp;lt;code>del&amp;lt;/code>
*&amp;lt;code>ins&amp;lt;/code>
*&amp;lt;code>map&amp;lt;/code>
*&amp;lt;code>object&amp;lt;/code>
*&amp;lt;code>script&amp;lt;/code>
*&amp;lt;code>Reference&amp;lt;/code>
*&amp;lt;code>[[css/properties/break-after|breakAfter]]&amp;lt;/code>
*&amp;lt;code>[[css/properties/break-before|breakBefore]]&amp;lt;/code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}