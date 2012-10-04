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
|Description=The following style rule will change the background color of any element that receives input focus:
|LiveURL=
|Code=
*:focus {
    background-color: #ffc;
} 
}}}}
{{Notes_Section
|Notes=
===Remarks===
In an HTML document, an element must receive focus from the user in order to become active and perform its tasks. For example, users must set input focus on a link in order to follow it. Similarly, users must give a '''TEXTAREA''' focus in order to enter text into it.
There are several ways to give focus to an element:
*Designate the element with a pointing device. Even elements that do not typically accept input, such as '''div''' and '''body''' elements, receive focus when clicked with the mouse.
*Navigate through the document with the TAB and Shift+TAB keys. The document's author may define a tabbing order that specifies the order in which elements will receive focus.
*Select an element through a [[html/attributes/accessKey|'''keyboard shortcut''']].

This pseudo-class requires that Windows Internet Explorer be in IE8 Standards mode rendering. For more information, see Defining Document Compatibility.
|Import_Notes=
===Syntax===

selector
:focus
===Parameters===
;''selector'':A CSS simple selector
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.11.3


}}
{{See_Also_Section
|Topic_clusters=Selectors, Pseudo-Classes
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}