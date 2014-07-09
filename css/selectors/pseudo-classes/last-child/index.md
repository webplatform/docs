{{Page_Title|:last-child}}
{{Flags
|State=Almost Ready
|Editorial notes=Fix broken links
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The <code>:last-child</code> pseudo-class represents the last child element of its parent.}}
{{CSS_Selector}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/*We add some red color to the second list item*/

li:last-child {
color: red;
}
|LiveURL=http://code.webplatform.org/gist/0b959135eaa76a5de965
}}{{Single Example
|Language=HTML
|Code=<ul>
	<li>I'm not red!</li>
	<li>I'm red!</li>
</ul>
}}
}}
{{Notes_Section
|Notes====Remarks===
The ''':last-child''' pseudo-class is a structural pseudo-class. Structural pseudo-classes enable selection based on extra information in the document tree that can't be selected using simple selectors or combinators.
|Import_Notes====Syntax===

selector
:last-child
===Parameters===
;''selector'':A CSS simple selector.
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199783 Selectors Level 3], Section 6.6.5.7
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
|Manual_sections====Related pages (MSDN)===
*<code>Reference</code>
*<code>[[css/selectors/pseudo-classes/:root|:root]]</code>
*<code>[[css/selectors/pseudo-classes/:nth-child(n)|:nth-child]]</code>
*<code>[[css/selectors/pseudo-classes/:nth-last-child(n)|:nth-last-child]]</code>
*<code>[[css/selectors/pseudo-classes/:nth-of-type(n)|:nth-of-type]]</code>
*<code>[[css/selectors/pseudo-classes/:nth-last-of-type(n)|:nth-last-of-type]]</code>
*<code>[[css/selectors/pseudo-classes/:first-of-type|:first-of-type]]</code>
*<code>[[css/selectors/pseudo-classes/:last-of-type|:last-of-type]]</code>
*<code>[[css/selectors/pseudo-classes/:only-child|:only-child]]</code>
*<code>[[css/selectors/pseudo-classes/:only-of-type|:only-of-type]]</code>
*<code>[[css/selectors/pseudo-classes/:empty|:empty]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}