{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections
|Content=Incomplete, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The :visited pseudo-class applies to links the user has visited}}
{{CSS_Selector
|Content=User agents commonly display unvisited links differently from previously visited ones. Selectors provides pseudo-classes to distinguish them:

* The <code>[[css/selectors/pseudo-classes/:link|:link]]</code> pseudo-class applies to links that have not yet been visited. 
* The <code>:visited</code> pseudo-class applies once the link has been visited by the user. 

After some amount of time, user agents may choose to return a visited link to the (unvisited) ‘<code>:link</code>’ state.

The two states are mutually exclusive.


}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The following style rule uses ''':visited''' to set the [[css/properties/color|'''color''']] attribute of visited links in a document.
|Code=a:visited { color:blue } 

}}
}}
{{Notes_Section
|Usage=''':visited'''  is often used with [[css/selectors/pseudo-classes/:active|''':active''']], [[css/selectors/pseudo-classes/:hover|''':hover''']], and [[css/selectors/pseudo-classes/:link|''':link''']], which are the pseudo-classes that reflect the other states of a link.
The default value of the ''':visited''' pseudo-class varies by browser, as does the amount of time used to define a recent visit.

|Notes=The pseudo-classes :link and :visited can be abused to determine which sites a user has visited.

To preserver their users privacy, browsers often implement  measures to preserve the user's privacy while rendering visited and unvisited links differently.
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
|Version=8.0
|Note=For security reasons, ''':visited''' is not supported by [[css/selectors api/querySelector|'''querySelector''']] or [[css/selectors api/querySelectorAll|'''querySelectorAll''']]
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