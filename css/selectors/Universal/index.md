{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes={{Editorial/Merge_Candidate
|Other=css/selectors/universal_selector}}
|Checked_Out=No
|High-level issues=Missing Relevant Sections, Needs Topics, Merge Candidate, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS_Selector}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following style rule draws a thin orange border around every element on the page.
|Code=&lt;style&gt;
    * { border: 1px solid orange; }
&lt;/style&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
The universal selector matches every element in the document tree. If the universal selector is not the only component of a simple selector, the "*" may be omitted. For example:
* *.myclass and .myclass are equivalent.
* *#myid and #myid are equivalent.
* *:hover and :hover are equivalent.
|Import_Notes====Syntax===
<code>'''*''' {...}</code>
===Parameters===
This (*) selector has no parameters.
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.3
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
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