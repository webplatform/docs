{{Page_Title|&#58;link}}
{{Flags
|High-level issues=Missing Relevant Sections
|Content=Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section}}
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
|Description=The following style rule uses the ''':link''' pseudo-class to set the default [[css/properties/color|'''color''']] attribute of a link in a document.
|Code=&lt;style&gt;
    A:link { color:#FF0000 }
&lt;/style&gt;
}}
}}
{{Notes_Section
|Usage=The ''':link''' pseudo-class is often used with [[css/selectors/pseudo-classes/:active|''':active''']], [[css/selectors/pseudo-classes/:hover|''':hover''']] and [[css/selectors/pseudo-classes/:visited|''':visited''']], the pseudo-classes that affect the other states of a link.
The default value of the ''':link''' pseudo-class is browser-specific. The time period used to define a recent visit also varies by browser.
|Notes=<blockquote>'''Note:''' It is possible for style sheet authors to abuse the :link and :visited pseudo-classes to determine which sites a user has visited without the user's consent. </blockquote>

UAs may therefore treat all links as unvisited links, or implement other measures to preserve the user's privacy while rendering visited and unvisited links differently.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS 2.1
|URL=http://www.w3.org/TR/CSS2/selector.html#link-pseudo-classes
|Status=W3C Recommendation
}}{{Related Specification
|Name=Selectors Level 3
|URL=http://www.w3.org/TR/css3-selectors/#link
|Status=W3C Recommendation
}}{{Related Specification
|Name=Selectors Level 4
|URL=http://dev.w3.org/csswg/selectors4/#link
|Status=W3C Working Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=3.0
|Note=Microsoft Internet Explorer 3.0 applies the value of the ''':link''' pseudo-class to the [[css/selectors/pseudo-classes/:visited|''':visited''']] pseudo-class.
}}
}}
{{See_Also_Section
|Topic_clusters=Selectors, Pseudo-Classes
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}