{{Page_Title|&#58;&#58;before}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs spec reference, remove topic cluster flags
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|<code>::before</code> creates a pseudo-element, which allows you to insert content onto a page from CSS before the selected element(s). The end result isn't actually in the DOM, but it appears on the page as if it is. The pseudo-element is inline by default.}}
{{CSS_Selector}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=p::before {
  content: 'Hello!';
}
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''::before''' and [[:css/selectors/pseudo-elements/::after|'''::after''']] pseudo-elements specify the location of content before and after an element in the document tree. The [[css/properties/content|'''content''']] attribute, in conjunction with these pseudo-elements, specifies what is inserted.
The generated content interacts with other boxes as if they were real elements inserted just inside their associated element. The content box of the associated element expands to include the generated content, if necessary.
In Windows Internet Explorer 8, as well as later versions of Windows Internet Explorer in IE8 Standards mode, only the one-colon form of this pseudo-element is recognized—that is, ''':before'''.
Beginning with Windows Internet Explorer 9, the '''::before''' pseudo-element requires two colons, though the one-colon form is still recognized and behaves identically to the two-colon form. Microsoft and the World Wide Web Consortium (W3C) encourage web authors to use the two-colon form of the '''::before''' pseudo-element. For more information, see the [http://go.microsoft.com/fwlink/p/?LinkId{{=}}241611 Pseudo-elements] section of the W3C's [http://go.microsoft.com/fwlink/p/?LinkId{{=}}241612 CSS3 Selectors] specification.
|Import_Notes====Parameters===
;''sel'':A simple selector.
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.12.3
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=4.0
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=2.0
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=8.0
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=9.0
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=3.1
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=2.1
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=7.0
|Blackberry_prefixed_supported=No
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=18.0
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=15.0
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=No
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=10.0
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_version=5.0
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=3.2
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Pseudo-Elements, Selectors
|Manual_sections====Related pages (MSDN)===
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