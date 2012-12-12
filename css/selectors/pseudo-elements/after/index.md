{{Page_Title|&#58;&#58;after}}
{{Flags
|High-level issues=Data Not Semantic
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Inserts content after the selected element(s).}}
{{CSS_Selector
|Content=The [[:css/selectors/pseudo-elements/::before|'''::before''']] and '''::after''' pseudo-elements specify the location of content before and after an element in the document tree. The [[css/properties/content|'''content''']] attribute, in conjunction with these pseudo-elements, specifies what is inserted.
The generated content interacts with other boxes as if they were real elements inserted just inside their associated element. The content box of the associated element expands to include the generated content, if necessary.

===Syntax===

sel
'''::after'''
===Parameters===
;''sel'':A simple selector
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=Web authors are encouraged to use the two-colon form of the '''::after''' pseudo-element.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS 2.1
|URL=http://www.w3.org/TR/CSS2/
|Status=W3C Recommendation
}}{{Related Specification
|Name=Selectors Level 3
|URL=http://www.w3.org/TR/css3-selectors/
|Status=W3C Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=8+
|Note=In Windows Internet Explorer 8, as well as later versions of Windows Internet Explorer in IE8 Standards mode, only the one-colon form of this pseudo-element is recognized—that is, ''':after'''. Beginning with Windows Internet Explorer 9, the '''::after''' pseudo-element requires two colons, though the one-colon form is still recognized and behaves identically to the two-colon form.
}}
}}
{{See_Also_Section
|Topic_clusters=Pseudo-Elements, Selectors
|Manual_sections====Related pages===
*<code>[[css/properties/content|content]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}