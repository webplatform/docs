{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|In typography terms, an orphan is the first line of a paragraph that is left behind on the old page while the paragraph continues on the next. The orphans CSS property refers to the minimum number of lines in a block container that must be left at the bottom of the old page. This property is normally used to control how page breaks occur. This property only affects paged media such as print. 

}}
{{CSS Property
|Initial value=2
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Computed value=As specified
|Animatable=No
|Values={{CSS Property Value
|Data Type=integer
|Description=Only positive values are allowed.
A '''String''' that specifies or receives the minimum number of lines to print at the bottom of a page.
}}{{CSS Property Value
|Data Type=inherit
|Description=Takes the same specified value as the property for the element's parent.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following style rule ensures that at least three lines
of a paragraph appear at the bottom and top of each printed page.
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
This property applies when the document is printed. If there are
fewer lines than necessary to satisfy this rule, the lines are
moved to the following page. The
[[css/properties/widows|'''widows''']]
attribute takes precedence over the
'''orphans''' attribute.
This property requires Windows Internet Explorer to be in
IE8 Standards mode rendering.
|Import_Notes====Syntax===
<code>'''orphans: '''integer</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 13.3
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Level 2 (Revision 1)
|URL=http://www.w3.org/TR/CSS2/page.html#propdef-orphans
|Status=Reccomendation
}}{{Related Specification
|Name=CSS Paged Media Module Level 3
|URL=http://dev.w3.org/csswg/css-page/#orphans
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
|Topic_clusters=Paged Media
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[css/properties/widows|widows]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}