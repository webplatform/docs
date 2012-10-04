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
|Description=The following style rule uses the ''':link''' pseudo-class to set the default [[css/properties/color|'''color''']] attribute of a link in a document.
|LiveURL=
|Code=
&lt;style&gt;
    A:link { color:#FF0000 }
&lt;/style&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The ''':link''' pseudo-class is often used with [[css/selectors/pseudo-classes/:active|''':active''']], [[css/selectors/pseudo-classes/:hover|''':hover''']] and [[css/selectors/pseudo-classes/:visited|''':visited''']], the pseudo-classes that affect the other states of a link.
The default value of the ''':link''' pseudo-class is browser-specific. The time period used to define a recent visit also varies by browser.
Microsoft Internet Explorer 3.0 applies the value of the ''':link''' pseudo-class to the [[css/selectors/pseudo-classes/:visited|''':visited''']] pseudo-class.
|Import_Notes=
===Syntax===

selector
:link
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