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
|Examples=}}
{{Notes_Section
|Notes=
===Remarks===
The '''::before''' and [[css/selectors/pseudo-elements/::after|'''::after''']] pseudo-elements specify the location of content before and after an element in the document tree. The [[css/properties/content|'''content''']] attribute, in conjunction with these pseudo-elements, specifies what is inserted.
The generated content interacts with other boxes as if they were real elements inserted just inside their associated element. The content box of the associated element expands to include the generated content, if necessary.
In Windows Internet Explorer 8, as well as later versions of Windows Internet Explorer in IE8 Standards mode, only the one-colon form of this pseudo-element is recognized—that is, ''':before'''.
Beginning with Windows Internet Explorer 9, the '''::before''' pseudo-element requires two colons, though the one-colon form is still recognized and behaves identically to the two-colon form. Microsoft and the World Wide Web Consortium (W3C) encourage web authors to use the two-colon form of the '''::before''' pseudo-element. For more information, see the [http://go.microsoft.com/fwlink/p/?LinkId{{=}}241611 Pseudo-elements] section of the W3C's [http://go.microsoft.com/fwlink/p/?LinkId{{=}}241612 CSS3 Selectors] specification.
|Import_Notes=
===Syntax===

sel
::before
===Parameters===
;''sel'':A simple selector.
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.12.3


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/properties/content|content]]</code>
|Topic_clusters=Selectors, Pseudo-Elements
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}