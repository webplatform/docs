{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Border-collapse can be used for collapsing the borders between table cells.}}
{{CSS Property
|Applies to=All elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=separate
|Description=Default. Borders are detached (standard HTML).
}}{{CSS Property Value
|Data Type=collapse
|Description=Borders are collapsed, where adjacent, into a single border.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example demonstrates how to use the '''border-collapse''' attribute and the '''border-collapse''' property to manipulate the border on a table.
|Code=&lt;table id{{=}}"oID_1" style{{=}}"border-collapse: collapse"&gt;
        &lt;tr&gt;
            &lt;td&gt;EST&lt;/td&gt;
            &lt;td&gt;9:00 a.m.&lt;/td&gt;
        &lt;/tr&gt;
        &lt;tr&gt;
            &lt;td&gt;CST&lt;/td&gt;
            &lt;td&gt;8:00 a.m.&lt;/td&gt;
        &lt;/tr&gt;
        &lt;tr&gt;
            &lt;td&gt;PST&lt;/td&gt;
            &lt;td&gt;6:00 a.m.&lt;/td&gt;
        &lt;/tr&gt;
    &lt;/table&gt;
    &lt;p&gt;
    &lt;input type{{=}}"button" onclick{{=}}"oID_1.style.borderCollapse{{=}}'separate'" value{{=}}"separate"&gt;
    &lt;input type{{=}}"button" onclick{{=}}"oID_1.style.borderCollapse{{=}}'collapse'" value{{=}}"collapse"&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/borderCollapse.htm
}}
}}
{{Notes_Section
|Import_Notes====Syntax===
<code>'''border-collapse: '''collapse '''{{!}}''' separate</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1]
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
|Topic_clusters=Tables
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[css/properties/border|border]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}