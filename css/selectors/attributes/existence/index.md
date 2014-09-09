{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs summary, spec reference, standardization status, remove topic cluster flags
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS_Selector
|Content=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following style rule selects any element with an "attr" attribute whose value is exactly "Value".
|Code=&lt;!DOCTYPE html&gt;
&lt;html&gt;
  &lt;head&gt;
    &lt;style type{{=}}"text/css"&gt;
      .test          { display:none; }
      [attr{{=}}"Value"] { display:block; }
    &lt;/style&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;div class{{=}}"test" attr{{=}}"Value"&gt;Test for [{{=}}] (Value) succeeded.&lt;/div&gt;
  &lt;/body&gt;
&lt;/html&gt;
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
'''Note'''  Requires Windows Internet Explorer 7 or later.
'''Note'''  Attribute selectors are not supported in webpages that are displayed in the Microsoft Internet Explorer 5 document mode (also known as "Quirks" mode). To use attribute selectors, add a [[html/elements/!DOCTYPE|!DOCTYPE]] directive that specifies a standard-based document. For more information, see [http://go.microsoft.com/fwlink/p/?LinkID{{=}}125785 Defining Document Compatibility].
Attributes are case-sensitive.
|Import_Notes====Syntax===
<code>
[''sel''=''att''] {...}
</code>

===Parameters===
* ''sel'': A selector.
* ''att'': Must be either an Identifier or a String.
* "=": An equality expression, one of <code>~=</code>, <code>^=</code>, <code>$=</code>, <code>*=</code>

===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199783 Selectors Level 3], Section 6.3
}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Topic_clusters=CSS Attributes, Selectors
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
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
|Opera_supported=Yes
|Opera_version=7+
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}