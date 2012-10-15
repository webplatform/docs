{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS_Selector}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=For example, the following style rule matches any [[html/elements/p|p]] element whose class attribute has been assigned a space-separated list of values that include the "pastoral" and "marine" class names. This rule matches when class{{=}}"pastoral aqua marine" but does not match when class{{=}}"pastoral blue".
|Code=&lt;style&gt;
    p.pastoral.marine { color: lightseagreen; }
&lt;/style&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
The class attribute value must immediately follow the "period" (.) notation. More than one class name can be specified in one style rule; to match a subset of class values, each value must be preceded by a period.
|Import_Notes====Syntax===
<code><strong/>''sel'''''.'''''value'' {...}
</code>
===Parameters===
;''sel'':Selector
;''value'':String that specifies the value of the "class" attribute.
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 1.4
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
|Topic_clusters=Selectors
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}