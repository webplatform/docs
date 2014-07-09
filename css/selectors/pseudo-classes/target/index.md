{{Page_Title|&#58;target}}
{{Flags
|State=Not Ready
|Editorial notes=Merge with [[CSS/Selectors/pseudo-classes/:target]]
|Checked_Out=No
|High-level issues=Missing Relevant Sections, Needs Topics, Merge Candidate, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS_Selector}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following selects the '''div''' element of class important that is the target element of the referring URI. If the document's URI has no fragment identifier, there is no target element.
|LiveURL=<pre xml:space{{=}}"preserve"><code>div.important:target</code></pre>
}}
}}
{{Notes_Section
|Notes====Remarks===
The ''':target''' pseudo-class selects the target element of the referring URI. A fragment identifier is used to identify a location within a document, and is formed using a number sign followed by an anchor identifier—for example, http://www.example.com/mypage.html#section_3.
|Import_Notes====Syntax===

selector
:target
===Parameters===
;''selector'':A CSS simple selector.
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199783 Selectors Level 3], Section 6.6.2
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
|Topic_clusters=Pseudo-Classes, Selectors
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}