{{Page_Title|&#58;link}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Missing Relevant Sections, Needs Review
|Content=Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Used to select and style unvisited links.}}
{{CSS_Selector
|Content=User agents commonly display unvisited links differently from previously visited ones. Selectors provides pseudo-classes to distinguish them:

* The :link pseudo-class applies to links that have not yet been visited.
* The [[css/selectors/pseudo-classes/:visited|:visited]] pseudo-class applies once the link has been visited by the user. 

After some amount of time, user agents may choose to return a visited link to the (unvisited) ‘:link’ state.

The two states are mutually exclusive.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The following style rule uses the ''':link''' pseudo-class to set the default [[css/properties/color|'''color''']] attribute of a link in a document.
|Code=&lt;style&gt;
    A:link { color:#FF0000 }
&lt;/style&gt;
|LiveURL=
}}
}}
{{Notes_Section
|Usage=The ''':link''' pseudo-class is often used with [[css/selectors/pseudo-classes/:active|''':active''']], [[css/selectors/pseudo-classes/:hover|''':hover''']] and [[css/selectors/pseudo-classes/:visited|''':visited''']], the pseudo-classes that affect the other states of a link.
The default value of the ''':link''' pseudo-class is browser-specific. The time period used to define a recent visit also varies by browser.
|Notes=<blockquote>'''Note:''' It is possible for style sheet authors to abuse the :link and :visited pseudo-classes to determine which sites a user has visited without the user's consent. </blockquote>

UAs may therefore treat all links as unvisited links, or implement other measures to preserve the user's privacy while rendering visited and unvisited links differently.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS 2.1
|URL=http://www.w3.org/TR/CSS2/selector.html#link-pseudo-classes
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related Specification
|Name=Selectors Level 3
|URL=http://www.w3.org/TR/css3-selectors/#link
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related Specification
|Name=Selectors Level 4
|URL=http://dev.w3.org/csswg/selectors4/#link
|Status=W3C Working Draft
|Relevant_changes=
}}
}}
{{See_Also_Section
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
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=3.0
|Note=Microsoft Internet Explorer 3.0 applies the value of the ''':link''' pseudo-class to the [[css/selectors/pseudo-classes/:visited|''':visited''']] pseudo-class.
}}
}}