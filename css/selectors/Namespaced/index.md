{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs title, summary, spec reference, standardization status, remove topic cluster flags
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS_Selector}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description='''Type''' selectors allow an optional namespace component (namespace prefix). The namespace prefix can be left empty to indicate that the selector is only to match elements with no namespace, or an asterisk can be used to indicate that the selector matches elements in any namespace (as well as elements with no namespace).
|Code=@namespace myprfx url(http://www.microsoft.com);
|LiveURL=First, declare the namespace prefix (<code>myprfx</code> in this example):
}}
}}
{{Notes_Section
|Notes====Remarks===
A ''CSS qualified name'' is an element or attribute name that is located within a namespace. To form a qualified name, first declare a namespace prefix by using the [[css/atrules/@namespace|'''@namespace''']] at-rule. Then, prepend the namespace prefix to the element or attribute name, separating the prefix and the name with a vertical bar ({{!}}).
'''Type''', universal, and attribute selectors can be namespaced, as shown in Examples.
|Import_Notes====Syntax===
<code><strong/>''prfx'''''{{!}}'''''selector'' {...}
</code>
===Parameters===
;''prfx'':A namespace prefix. The namespace prefix is declared by the [[css/atrules/@namespace|'''@namespace''']] at-rule.
;''selector'':A local element or attribute name.
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199777 CSS Namespaces Module], Section 4
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