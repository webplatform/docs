{{Page_Title|&#58;focus}}
{{Flags
|State=Almost Ready
|Editorial notes=Fix broken links, remove topic cluster flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The ''':focus''' pseudo-class applies while an element has the focus, i.e. accepts keyboard or mouse events, or other forms of input.}}
{{CSS_Selector
|Content=In an HTML document, an element must receive focus from the user in order to become active and perform its tasks. For example, users must set input focus on a link in order to follow it. Similarly, users must give a [[html/elements/textarea|textarea]] focus in order to enter text into it.

There are several ways to give focus to an element:
* Designate the element with a pointing device. Even elements that do not typically accept input, such as '''[[html/elements/div|div]]''' and '''[[html/elements/body|body]]''' elements, receive focus when clicked with the mouse.
* Navigate through the document with the TAB and Shift+TAB keys. The document’s author may define a tabbing order that specifies the order in which elements will receive focus with the [[html/attributes/tabindex|tabindex]] attribute.
* Select an element through a [[html/attributes/accessKey|'''keyboard shortcut''']].
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The following style rule will change the background color of any element that receives input focus:
|Code=*:focus {
    background-color: #ffc;
}
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
|Name=CSS 2.1
|URL=http://www.w3.org/TR/CSS2/selector.html#link-pseudo-classes
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related Specification
|Name=Selectors Level 3
|URL=http://www.w3.org/TR/css3-selectors/#the-user-action-pseudo-classes-hover-act
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related Specification
|Name=Selectors Level 4
|URL=http://dev.w3.org/csswg/selectors4/#focus-pseudo
|Status=W3C Working Draft
|Relevant_changes=
}}
}}
{{See_Also_Section
|Topic_clusters=Pseudo-Classes, Selectors
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
|Desktop_rows=
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=8
|Note=This pseudo-class requires that Windows Internet Explorer be in IE8 Standards mode rendering.
}}
}}