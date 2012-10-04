{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_At_Rule
|Content=
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example implements the '''@charset''' rule.
|LiveURL=
|Code=
@charset "Windows-1251";
}}}}
{{Notes_Section
|Notes=
===Remarks===
Dynamic HTML (DHTML) expressions can be used in place of the preceding value(s). As of Windows Internet Explorer 8, expressions are not supported in IE8 Standards mode. For more information, see About Dynamic Properties.
The rule has no default value.
You can use only one '''@charset''' rule in an external style sheet.  The rule must appear at the top of the file, cannot be preceded by any characters, and cannot be included in an embedded style sheet.
|Import_Notes=
===Syntax===
<code>'''@charset '''''CharSet-Description''</code>
===Parameters===
;''CharSet-Description'':'''String''' that specifies the HTML Character Sets.
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 4.4


}}
{{See_Also_Section
|Topic_clusters=Syntax
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}