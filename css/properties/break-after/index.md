{{Page_Title|break-after}}
{{Flags
|Content=Examples Needed, Needs Summary
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The CSS break-after property allows you to force a break on multi-column layouts. More specifically, it allows you to force a break after an element. It allows you to determine if a break should occur, and what type of break it should be. The break-after CSS property describes how the page, column or region break behaves after the generated box. If there is no generated box, the property is ignored.}}
{{CSS Property
|Initial value=auto
|Applies to=block-level elements
|Inherited=No
|Media=visual
|Animatable=No
|CSS object model property=breakAfter
|Values={{CSS Property Value
|Data Type=auto
|Description=Default. A page break or column break is determined  by the flow of content.

}}{{CSS Property Value
|Data Type=always
|Description=A page/column/region break is inserted (forced) after the content block.

}}{{CSS Property Value
|Data Type=avoid
|Description=A page/column/region break is not allowed after the content block.

}}{{CSS Property Value
|Data Type=left
|Description=A page break is inserted (forced) after the content block, causing the flow of content to continue in the first column of the "left" page that immediately follows the current page (according to the paging format of the document).
}}{{CSS Property Value
|Data Type=right
|Description=A page break is inserted (forced) after the content block, causing the flow of content to continue in the first column of the "right" page that immediately follows the current page (according to the paging format of the document).
}}{{CSS Property Value
|Data Type=page
|Description=A page break is inserted (forced) after the content block, causing the flow of content to continue in the first column of the page that immediately follows the current page (according to the paging format of the document).
}}{{CSS Property Value
|Data Type=column
|Description=A column break is inserted (forced) after the content block.
}}{{CSS Property Value
|Data Type=avoid-page
|Description=A page break is not allowed after the content block.
}}{{CSS Property Value
|Data Type=avoid-column
|Description=A column break is not allowed after the content block.
}}{{CSS Property Value
|Data Type=region
|Description=A [[css/concepts/region|region]] break is inserted (forced) after the content block.
}}{{CSS Property Value
|Data Type=avoid-region
|Description=A [[css/concepts/region|region]] break is not allowed after the content block.
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
}}{{Single Example
|Language=CSS
|Code=.multicol {
background-color:lightyellow;
padding:20px;

/* CSS3 */
column-count: 3; 
column-rule: 5px dotted coral;
vertical-align:text-top;
}

.multicol hr {
break-after: column;
}
|LiveURL=http://code.webplatform.org/gist/7281550
}}
}}
{{Notes_Section
|Usage=The break-after property is not supported for absolutely positioned elements.

This property replaces separate '''column-break-after''', '''page-break-after''', and '''region-break-after''' properties, which may still be present in some browser implementations.
|Notes=The break-after property is ignored if there is no generated box or flows defined. So most of the times, you have to define a flow of content to test the property.
|Import_Notes=Each possible break point, that is each element boundary, is under the influence of three properties, the break-after value of the previous element, the break-before value of the next element and the break-inside of the containing element.

To define if a break must be done, the following rules are applied:

If any of the three concerned values is a forced break value, that is always, left, right, page, column or region, it has precedence. If several of the concerned values is such a break, the one of the element that appears the latest in the flow is taken (that is the break-before value has precedence over the break-after value, which itself has precedence over the break-inside value).

If any of the three concerned values is an avoid break value, that is avoid, avoid-page, avoid-region, avoid-column, no such break will be applied at that point.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Regions Module Level 3
|URL=http://www.w3.org/TR/css3-regions/#region-flow-break
|Status=Working Draft
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
|External_links=* W3C editor's draft: [http://dev.w3.org/csswg/css3-regions/ CSS Regions Module Level 3]
* Adobe Web Standards: [http://html.adobe.com/webstandards/cssregions CSS Regions]
* Adobe Developer's Network: [http://www.adobe.com/devnet/html5/articles/css3-regions.html CSS3 Regions: Rich page layout with HTML and CSS3]
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
*<code>[[css/properties/break-before|breakBefore]]</code>
*<code>[[css/properties/break-inside|breakInside]]</code>
}}
{{Topics|CSS, CSS-Regions}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}