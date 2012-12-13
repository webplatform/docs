{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Imports an external style sheet.}}
{{CSS_At_Rule}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example uses the '''@import''' rule to import a style sheet. For the example to work, you must replace <code>URL</code> in the example code with the address of a style sheet.
|Code=&lt;STYLE TYPE{{=}}"text/css"&gt;
    @import url("URL");
    P {color:blue}
&lt;/STYLE&gt;
}}{{Single Example
|Description=The following example, without <code>url()</code>, has the same effect as the previous example.
|Code=&lt;STYLE type{{=}}"text/css"&gt;
    @import "URL";
    P {color:blue}
&lt;/STYLE&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
The rule has no default value.
The semicolon in the syntax is required; if omitted, the style sheet is not imported properly and an error message is generated.  "url()" is optional because there is always a URL following "@import."
The '''@import''' rule, like the '''link''' element, links an external style sheet to a document. This helps the Web author establish a consistent "look" across
multiple HTML pages. Whereas the '''link''' element specifies the name of the style sheet to import using its [[html/attributes/href|'''href''']]
attribute, the '''@import''' rule specifies the style sheet definition inside a '''link''' element or a '''style''' element. In the scripting model, this means the [[css/cssom/styleSheet/owningElement|'''owningElement''']] property of the style sheet defined through the '''@import''' rule is either a '''style''' or a '''link''' object.
The '''@import''' rule should occur at the start of a style sheet, before any declarations.  You can place '''@import''' rule statements anywhere within the style sheet definition, but the rules contained within the '''@import''' rule style sheet are applied to the document before any other rules defined for the containing style sheet. This rule order affects expected rendering.
Rules in the style sheet override rules in the imported style sheet.
|Import_Notes====Syntax===
@import
===Parameters===
;''sUrl'':String that specifies the URL that references a cascading style sheet.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS 2.1, section 6.3
|URL=http://www.w3.org/TR/CSS2/cascade.html#at-import
|Status=W3C Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Unknown
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=up to (but excluding) 8
|Note=Internet Explorer supports so called  Dynamic HTML (DHTML) expressions in place of URLs. As of Windows Internet Explorer 8, expressions are not supported in IE8 Standards mode. For more information, see About Dynamic Properties in MSDN.
}}
}}
{{See_Also_Section
|Topic_clusters=CSS Layout, Syntax
|Manual_sections====Related pages===
*<code>[[css/cssom/imports|imports]]</code>
*<code>[[css/selectors/pseudo-classes/:link|:link]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[css/cssom/styleSheet|styleSheet]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}