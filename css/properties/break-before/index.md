{{Page_Title}}
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
|Description=Default. A page break or column break is determined  by the flow of content.
}}{{CSS Property Value
|Data Type=always
|Description=A page break is inserted (forced) before the content block.
}}{{CSS Property Value
|Data Type=avoid
|Description=A page/column/region break is not allowed before the content block.
}}{{CSS Property Value
|Data Type=left
|Description=A page break is inserted (forced) before the content block such that the flow of content continues in the first column of the "left" page that immediately follows the current page (according to the paging format of the document).
}}{{CSS Property Value
|Data Type=right
|Description=A page break is inserted (forced) before the content block such that the flow of content continues in the first column of the "right" page that immediately follows the current page (according to the paging format of the document).
}}{{CSS Property Value
|Data Type=page
|Description=A page break is inserted (forced) before the content block such that the flow of content continues in the first column of the page that immediately follows the current page (according to the paging format of the document).
}}{{CSS Property Value
|Data Type=column
|Description=A column break is inserted (forced) before the content block.
}}{{CSS Property Value
|Data Type=avoid-page
|Description=A page break is not allowed before the content block.
}}{{CSS Property Value
|Data Type=avoid-column
|Description=A column break is not allowed before the content block.
}}{{CSS Property Value
|Data Type=region
|Description=A region break is inserted (forced) before the content block.
}}{{CSS Property Value
|Data Type=avoid-region
|Description=A region break is not allowed before the content block.
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
<code>'''break-before: '''auto '''{{!}}''' always '''{{!}}''' avoid '''{{!}}''' left '''{{!}}''' right '''{{!}}''' page '''{{!}}''' column '''{{!}}''' avoid-page '''{{!}}''' avoid-column</code>
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
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Multi-Column, Regions
|Manual_links=* [[tutorials/css-regions|Using CSS Regions to flow content through a layout]]
|External_links=* [http://html.adobe.com/webstandards/cssregions Adobe Web Standards: CSS Regions]
* [http://www.adobe.com/devnet/html5/articles/css3-regions.html CSS3 regions: Rich page layout with HTML and CSS3]
* [http://adobe.github.com/web-platform/samples/css-regions Sample pages]
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>address</code>
*<code>blockQuote</code>
*<code>div</code>
*<code>dl</code>
*<code>fieldSet</code>
*<code>form</code>
*<code>noFrames</code>
*<code>noScript</code>
*<code>ol</code>
*<code>p</code>
*<code>pre</code>
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
*<code>[[css/properties/break-inside|breakInside]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}