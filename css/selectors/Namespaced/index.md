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
|Description='''Type''' selectors allow an optional namespace component (namespace prefix). The namespace prefix can be left empty to indicate that the selector is only to match elements with no namespace, or an asterisk can be used to indicate that the selector matches elements in any namespace (as well as elements with no namespace).
|LiveURL=First, declare the namespace prefix (<code>myprfx</code> in this example):
|Code=
@namespace myprfx url(http://www.microsoft.com);
}}}}
{{Notes_Section
|Notes=
===Remarks===
A ''CSS qualified name'' is an element or attribute name that is located within a namespace. To form a qualified name, first declare a namespace prefix by using the [[css/atrules/@namespace|'''@namespace''']] at-rule. Then, prepend the namespace prefix to the element or attribute name, separating the prefix and the name with a vertical bar ({{!}}).
'''Type''', universal, and attribute selectors can be namespaced, as shown in Examples.
|Import_Notes=
===Syntax===
<code><strong/>''prfx'''''{{!}}'''''selector'' {...}
</code>
===Parameters===
;''prfx'':A namespace prefix. The namespace prefix is declared by the [[css/atrules/@namespace|'''@namespace''']] at-rule.
;''selector'':A local element or attribute name.
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199777 CSS Namespaces Module], Section 4


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