{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS Property
|Initial value=0
|Applies to=All elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=integer
|Description=A '''String''' that specifies or receives 
the minimum number of lines to print at the bottom of a page.
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
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
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