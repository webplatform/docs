{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The widows CSS property defines how many minimum lines must be left on top of a new page, on a paged media. In typography, a widow is the last line of a paragraph appearing alone at the top of a page. Setting the widows property allows to prevent widows to be left.

On a non-paged media, like screen, the widows CSS property has no effect.
It can have a number value or it can inherit the values from the parent element.
}}
{{CSS Property
|Initial value=2
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Computed value=As specified
|Animatable=No
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=integer
|Description=Denotes the minimum amount of lines that can stay alone on the top of a new page. If the value is not positive, the declaration is invalid.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following style rule ensures that at least three lines
of a paragraph appear at the bottom and top of each printed document.
|Code=&lt;meta http-equiv{{=}}"X-UA-Compatible" content{{=}}"IE{{=}}8" /&gt;
&lt;style type{{=}}"text/css"&gt;
@media print {
    p {
        widows:3;
        orphans:3;
    }
}
&lt;/style&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
This property applies when the document is printed.
If there are fewer lines than necessary to satisfy this rule,
the lines are moved to the following document. The
'''widows'''
property has precedence over the
[[css/properties/orphans|'''orphans''']] property.
This property requires Windows Internet Explorer to be in
IE8 Standards mode rendering.
|Import_Notes====Syntax===
<code>'''widows: '''integer</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 13.3
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Fragmentation Module Level 3
|URL=http://dev.w3.org/csswg/css-break/#widows-orphans
|Status=Working Draft
}}{{Related Specification
|Name=CSS Multi-column Layout Module
|URL=http://dev.w3.org/csswg/css-multicol/#filling-columns
|Status=Candidate Reccomendation
}}{{Related Specification
|Name=CSS Level 2 (Revision 1)
|URL=http://www.w3.org/TR/CSS2/page.html#break-inside
|Status=Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=No
|Chrome_version=
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=8.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Yes
|Opera_prefixed_version=9.2
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Paged Media
|External_links=http://xhtml.com/en/css/reference/widows/
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[css/properties/orphans|orphans]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}