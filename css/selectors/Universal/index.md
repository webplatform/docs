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
|Description=The following style rule draws a thin orange border around every element on the page.
|LiveURL=
|Code=
&lt;style&gt;
    * { border: 1px solid orange; }
&lt;/style&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The universal selector matches every element in the document tree. If the universal selector is not the only component of a simple selector, the "*" may be omitted. For example:
**.myclass and .myclass are equivalent.
**#myid and #myid are equivalent.
**:hover and :hover are equivalent.

|Import_Notes=
===Syntax===
<code><strong/><em/>'''*'''<em/> {...}
</code>
===Parameters===
This (*) selector has no parameters.
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.3


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