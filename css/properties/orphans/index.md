{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_Property
|Applies to=All elements
|Media=visual
|Inherited=No
|Initial value=0
|Values={{CSS_Property_Value|Data Type=integer |Description=A '''String''' that specifies or receives 
the minimum number of lines to print at the bottom of a page.}}
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following style rule ensures that at least three lines
of a paragraph appear at the bottom and top of each printed page.
|LiveURL=
|Code=
&lt;meta http-equiv{{=}}"X-UA-Compatible" content{{=}}"IE{{=}}8" /&gt;
&lt;style type{{=}}"text/css"&gt;
@media print {
    p {
        widows:3;
        orphans:3;
    }
}
&lt;/style&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
This property applies when the document is printed. If there are
fewer lines than necessary to satisfy this rule, the lines are
moved to the following page. The
[[css/properties/widows|'''widows''']]
attribute takes precedence over the
'''orphans''' attribute.
This property requires Windows Internet Explorer to be in
IE8 Standards mode rendering.
|Import_Notes=
===Syntax===
<code>'''orphans: '''integer</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 13.3


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[css/properties/widows|widows]]</code>
|Topic_clusters=Paged Media
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}