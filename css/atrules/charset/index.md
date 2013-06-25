{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Specifies the character encoding of the style sheet.}}
{{CSS_At_Rule}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Set the character encoding of the style sheet to Unicode UTF-8 (recommended)
|Code=@charset "UTF-8";
}}{{Single Example
|Language=CSS
|Description=Set the character encoding of the style sheet to Cyrillic (Windows 1251)
|Code=@charset "Windows-1251";
}}
}}
{{Notes_Section
|Notes====Remarks===
You can use only one '''@charset''' rule in an external style sheet.  The rule must appear at the top of the file, cannot be preceded by any characters, and cannot be included in an embedded style sheet.

The rule has no default value.
|Import_Notes====Syntax===
<code>'''@charset '''''CharSet-Description''</code>
===Parameters===
;''CharSet-Description'':'''String''' that specifies the name of the character encoding.
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 4.4
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Cascading Style Sheets Level 2 Revision 1 (CSS 2.1)
|URL=http://www.w3.org/TR/CSS2/
|Status=Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Syntax
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}