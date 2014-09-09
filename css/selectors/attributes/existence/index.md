{{Page_Title|Attribute selector}}
{{Flags
|State=In Progress
|Editorial notes=Needs summary, spec reference, standardization status, remove topic cluster flags
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Allows to select tags that has an attributes. While it can match the class and the id selector, its specificity value is lower.}}
{{CSS_Selector
|Content====Syntax===
<code>
[''sel''=''att''] {...}
</code>

===Parameters===
* ''sel'': The name of a tag property
* ''att'': Must be either an Identifier or a String.
* "=": An equality expression, one of 
** <code>=</code>  Exactly equals,
** <code>^=</code>  Begins with, 
** <code>$=</code>  Ends with, 
** <code>~=</code>  Contains (with word boundary),
** <code>*=</code>  Contains (without word boundary)
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
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Selectors Level 3
|URL=http://www.w3.org/TR/css3-selectors/#attribute-selectors
|Status=W3C Recommendation
|Relevant_changes=
}}
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