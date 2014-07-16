{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|In typography terms, an orphan is the first line of a paragraph that is left behind on the old page while the paragraph continues on the next. The orphans CSS property refers to the minimum number of lines in a block container that must be left at the bottom of the old page. This property is normally used to control how page breaks occur. This property only affects paged media such as print.
For example, if a paragraph can't fit on one page in its entirety it is split wherever it is possible. In this way single lines of a paragraph can appear on page before it continues on the next page. This is usually unwanted, so many word processors require at least two lines to be left on an old page, instead of one. You can give it either a positive number (where 2 is the default) or inherit.

Note that the orphan property does not generally affect non-paged media such as screen. However, browsers supporting both orphans and columns will apply the intended functionality to columns as well. Also, the property only affects block-level elements.
}}
{{CSS Property
|Initial value=2
|Applies to=Block containers
|Inherited=Yes
|Media=visual
|Computed value=As specified
|Animatable=No
|CSS object model property=orphans
|Values={{CSS Property Value
|Data Type=integer
|Description=Only positive values are allowed.
An '''Integer''' that specifies or receives the minimum number of lines to print at the bottom of a page.
}}{{CSS Property Value
|Data Type=inherit
|Description=Takes the same specified value as the property for the element's parent.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The following style rule ensures that at least three lines
of a paragraph appear at the bottom and top of each printed page.
|Code=@media print {
    p {
        widows: 3;
        orphans: 3;
    }
}
}}
}}
{{Notes_Section
|Notes====Remarks===
The [[css/properties/widows|'''widows''']] property takes precedence over '''orphans'''.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Fragmentation Module Level 3
|URL=http://www.w3.org/TR/css3-break/#widows-orphans
|Status=W3C Working Draft
}}{{Related Specification
|Name=CSS Paged Media Module Level 3
|URL=http://dev.w3.org/csswg/css-page/#orphans
|Status=W3C Editor's Draft
}}{{Related Specification
|Name=CSS Level 2 (Revision 1)
|URL=http://www.w3.org/TR/CSS2/page.html#propdef-orphans
|Status=W3C Reccomendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=8
|Note=This property requires Windows Internet Explorer to be in IE8 Standards mode rendering.
}}
}}
{{See_Also_Section
|Manual_sections====Related pages ===
*<code>[[css/properties/widows|widows]]</code>
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}