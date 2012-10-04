{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_Selector
|Content=
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=For example, the following style rule matches any P element whose CLASS attribute has been assigned a space-separated list of values that include the "pastoral" and "marine" class names. This rule matches when class{{=}}"pastoral aqua marine" but does not match when class{{=}}"pastoral blue".
|LiveURL=
|Code=
&lt;style&gt;
    P.pastoral.marine { color: lightseagreen; }
&lt;/style&gt; 
}}}}
{{Notes_Section
|Notes=
===Remarks===
The CLASS attribute value must immediately follow the "period" (.) notation. More than one class name can be specified in one style rule; to match a subset of CLASS values, each value must be preceded by a period.
|Import_Notes=
===Syntax===
<code><strong/>''sel'''''.'''''value'' {...}
</code>
===Parameters===
;''sel'':Selector
;''value'':String that specifies the value of the "class" attribute.
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 1.4


}}
{{See_Also_Section
|Topic_clusters=Selectors
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}