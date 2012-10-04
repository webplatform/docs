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
|Description=The following style rule selects any element with an "attr" attribute whose value includes the substring "ai".
|LiveURL=
|Code=
&lt;!DOCTYPE html&gt;
&lt;html&gt;
  &lt;head&gt;
    &lt;style type{{=}}"text/css"&gt;
      .test        { display:none; }
      [attr*{{=}}"ai"] { display:block; }
    &lt;/style&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;div class{{=}}"test" attr{{=}}"Contains"&gt;Test for [*{{=}}] (Substring) succeeded.&lt;/div&gt;
  &lt;/body&gt;
&lt;/html&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
'''Note'''  Requires Windows Internet Explorer 7 or later.
'''Note'''  Attribute selectors are not supported in webpages that are displayed in the Microsoft Internet Explorer 5 document mode (also known as "Quirks" mode). To use attribute selectors, add a [[html/elements/!DOCTYPE|!DOCTYPE]] directive that specifies a standard-based document. For more information, see [http://go.microsoft.com/fwlink/p/?LinkID{{=}}125785 Defining Document Compatibility].
Attributes are case-sensitive.
|Import_Notes=
===Syntax===
<code><strong/>
[''att'''''*{{=}}'''''val'']
{...}</code>
===Parameters===
;''att'':Must be either an Identifier or a String.
;''val'':Must be either an Identifier or a String.
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199783 Selectors Level 3], Section 6.3


}}
{{See_Also_Section
|Topic_clusters=Selectors, CSS Attributes
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}