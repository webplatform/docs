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
|Description=The following style rule uses ''':visited''' to set the [[css/properties/color|'''color''']] attribute of visited links in a document.
|LiveURL=
|Code=
&lt;style&gt;
    A:visited { color:blue } 
&lt;/style&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
''':visited'''  is often used with [[css/selectors/pseudo-classes/:active|''':active''']], [[css/selectors/pseudo-classes/:hover|''':hover''']], and [[css/selectors/pseudo-classes/:link|''':link''']], which are the pseudo-classes that reflect the other states of a link.
The default value of the ''':visited''' pseudo-class varies by browser, as does the amount of time used to define a recent visit.
Windows Internet Explorer 8. For security reasons, ''':visited''' is not supported by [[css/selectors api/querySelector|'''querySelector''']] or [[css/selectors api/querySelectorAll|'''querySelectorAll''']];  for more information, see Selecting Objects with JavaScript.
|Import_Notes=
===Syntax===

selector
:visited
===Parameters===
;''selector'':A CSS simple selector.
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.11.2


}}
{{See_Also_Section
|Topic_clusters=Selectors, Pseudo-Classes
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}