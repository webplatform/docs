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
|Description=The following style rule uses the ''':active''' pseudo-class to set the [[css/properties/font-weight|'''font-weight''']] and [[css/properties/color|'''color''']] attributes of an active link in a document.
|LiveURL=
|Code=
&lt;style&gt;
    A:active { font-weight:bold; color:purple }
&lt;/style&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The default value of the ''':active''' pseudo-class is browser-specific.
The ''':active''' pseudo-class is most often used with the [[html/elements/a|'''a''']] element. Windows Internet Explorer 7 and earlier only support using the ''':active''' pseudo-class with the '''a''' element. "Active" means that the user is navigating the link.  The link has been activated, and some action is being performed but is not yet complete.
The ''':active''' pseudo-class is often used with [[css/selectors/pseudo-classes/:hover|''':hover''']], [[css/selectors/pseudo-classes/:link|''':link''']], and [[css/selectors/pseudo-classes/:visited|''':visited''']], the pseudo-classes that affect the other states of a link.
Dynamic HTML (DHTML) expressions can be used in place of the preceding value(s). As of Windows Internet Explorer 8, expressions are not supported in IE8 Standards mode. For more information, see About Dynamic Properties.
|Import_Notes=
===Syntax===

selector
:active
===Parameters===
;''selector'':A CSS simple selector
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.11.3


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