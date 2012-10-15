{{Page_Title}}
{{Flags
|Content=Compatibility Incomplete
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The :active pseudo-class applies while an element is being activated by the user.}}
{{CSS_Selector
|Content=The :active pseudo-class applies while an element is being activated by the user. For example, between the times the user presses the mouse button and releases it. On systems with more than one mouse button, :active applies only to the primary or primary activation button (typically the "left" mouse button), and any aliases thereof.


}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The following style rule uses the ''':active''' pseudo-class to set the [[css/properties/font-weight|'''font-weight''']] and [[css/properties/color|'''color''']] attributes of an active link in a document.
|Code=a:active { font-weight:bold; color:purple }

}}
}}
{{Notes_Section
|Usage=The ''':active''' pseudo-class is most often used with the [[html/elements/a|'''a''']] element.

The ''':active''' pseudo-class is often used with [[css/selectors/pseudo-classes/:hover|''':hover''']], [[css/selectors/pseudo-classes/:link|''':link''']], and [[css/selectors/pseudo-classes/:visited|''':visited''']], the pseudo-classes that affect the other states of a link.
|Notes=It is undefined if the parent of an element that is ‘:active’ or ‘:hover’ is also in that state. 

The default value of the ''':active''' pseudo-class is browser-specific.



}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS 2.1
|URL=http://www.w3.org/TR/CSS2/selector.html#dynamic-pseudo-classes
|Status=W3C Recommendation
}}{{Related Specification
|Name=Selectors Level 3
|URL=http://www.w3.org/TR/css3-selectors/#the-user-action-pseudo-classes-hover-act
|Status=W3C Recommendation
}}{{Related Specification
|Name=Selectors Level 4
|URL=http://dev.w3.org/csswg/selectors4/#active-pseudo
|Status=W3C Working Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=<= 7
|Note=Windows Internet Explorer 7 and earlier only support using the ''':active''' pseudo-class with the '''a''' element. "Active" means that the user is navigating the link.  The link has been activated, and some action is being performed but is not yet complete.
}}{{Compatibility Notes Row
|Browser=Internet Explorer
|Note=Dynamic HTML (DHTML) expressions can be used in place of the preceding value(s). As of Windows Internet Explorer 8, expressions are not supported in IE8 Standards mode. 
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