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
|Examples=}}
{{Notes_Section
|Notes=
===Remarks===
A descendant combinator is white space that separates two simple selectors. A selector of the form "E F" matches element F when it is an arbitrary descendant of some ancestor element E.
'''Note'''  Descendant combinators were called contextual selectors in Cascading Style Sheets, Level 1 (CSS1).
To skip over a generation of elements and pass styles to descendants beyond child elements, combine the Universal (*) Selector with the Descendant Combinator. For example, the following selector matches any '''p''' elements that are not direct descendants (grandchildren or later) of a '''div''' element.
<code>DIV * P {}</code>
|Import_Notes=
===Syntax===
<code>''first''''' '''''second'' { ... }
</code>
===Parameters===
;''first'':A CSS simple selector.
;''second'':A CSS simple selector.
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.5


}}
{{See_Also_Section
|Topic_clusters=Selectors, Combinators
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}