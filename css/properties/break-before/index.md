{{Page_Title|break-before}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The break-before property is used to break the flow of content before the generated box.}}
{{CSS Property
|Initial value=auto
|Applies to=block-level elements
|Inherited=No
|Computed value=specified value
|Animatable=No
|CSS object model property=breakBefore
|CSS percentages=n/a
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
}}{{Single Example
|Language=CSS
|Description=Forces h3s onto a new column.

|Code=h3 {
    break-inside: before;
    -webkit-column-break-inside: before;        
}
|LiveURL=http://code.webplatform.org/gist/6158525
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Regions Module Level 3
|URL=http://dev.w3.org/csswg/css3-regions/
|Status=W3C Working Draft
}}{{Related Specification
|Name=CSS Fragmentation Module Level 3
|URL=http://www.w3.org/TR/css3-break/#break-properties
|Status=W3C Working Draft
}}{{Related Specification
|Name=CSS Multi-column Layout Module
|URL=http://www.w3.org/TR/css3-multicol/#column-breaks
|Status=W3C Candidate Recommendation
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
|Topic_clusters=CSS Layout, Box Model, Flexbox, Multi-Column, Regions, Responsive Web Design, Shapes
|External_links=* Adobe Web Standards: [http://html.adobe.com/webstandards/cssregions CSS Regions]
* Adobe Developer's Network: [http://www.adobe.com/devnet/html5/articles/css3-regions.html CSS3 Regions: Rich page layout with HTML and CSS3]
* [http://adobe.github.com/web-platform/samples/css-regions Sample pages]
}}
{{Topics|CSS, CSS-Regions, Flexbox, UI}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}