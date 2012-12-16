{{Page_Title|break-inside property}}
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
|Description=A region break is not allowed within the content block.
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
&lt;code>'''break-inside: '''auto '''{{!}}''' avoid '''{{!}}''' avoid-page '''{{!}}''' avoid-column&lt;/code>
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
|External_links=* W3C editor's draft: [http://dev.w3.org/csswg/css3-regions/ CSS Regions Module Level 3]
* Adobe Web Standards: [http://html.adobe.com/webstandards/cssregions CSS Regions]
* Adobe Developer's Network: [http://www.adobe.com/devnet/html5/articles/css3-regions.html CSS3 Regions: Rich page layout with HTML and CSS3]
* [http://adobe.github.com/web-platform/samples/css-regions Sample pages]
|Manual_sections====Related pages (MSDN)===
*&lt;code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]&lt;/code>
*&lt;code>[[css/cssom/currentStyle|currentStyle]]&lt;/code>
*&lt;code>[[css/cssom/style|style]]&lt;/code>
*&lt;code>address&lt;/code>
*&lt;code>blockQuote&lt;/code>
*&lt;code>div&lt;/code>
*&lt;code>dl&lt;/code>
*&lt;code>fieldSet&lt;/code>
*&lt;code>form&lt;/code>
*&lt;code>noFrames&lt;/code>
*&lt;code>noScript&lt;/code>
*&lt;code>ol&lt;/code>
*&lt;code>p&lt;/code>
*&lt;code>pre&lt;/code>
*&lt;code>[[html/elements/table|table]]&lt;/code>
*&lt;code>ul&lt;/code>
*&lt;code>dd&lt;/code>
*&lt;code>dt&lt;/code>
*&lt;code>li&lt;/code>
*&lt;code>tBody&lt;/code>
*&lt;code>td&lt;/code>
*&lt;code>tFoot&lt;/code>
*&lt;code>th&lt;/code>
*&lt;code>tHead&lt;/code>
*&lt;code>tr&lt;/code>
*&lt;code>button&lt;/code>
*&lt;code>del&lt;/code>
*&lt;code>ins&lt;/code>
*&lt;code>map&lt;/code>
*&lt;code>object&lt;/code>
*&lt;code>script&lt;/code>
*&lt;code>Reference&lt;/code>
*&lt;code>[[css/properties/break-after|breakAfter]]&lt;/code>
*&lt;code>[[css/properties/break-before|breakBefore]]&lt;/code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}