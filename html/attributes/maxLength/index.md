{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|This article outlines the HTML attribute "maxlength," which ensures the number of characters entered in an HTML element is not greater than the value specified by this attribute.}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Code=<form action="demo_form.asp">
  Username: <input type="text" name="usrname" maxlength="10"><br>
  <input type="submit" value="Submit">
</form>
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''maxLength''' property limits the number of characters the user can enter. The property does not limit programmatic assignments to the [[html/attributes/value (button element)|'''value''']] property. The property's value can be larger than the [[html/attributes/size (control)|'''size''']] of the text box, in which case the text box scrolls as the user types.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 2.5.5
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 17.4
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 4.10.7.3.8
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Unknown
|Android_version=
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=9
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Unknown
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=HTML, Text
|Manual_sections====Related pages (MSDN)===
*<code>input type{{=}}text</code>
*<code>input type{{=}}password</code>
*<code>[[dom/HTMLInputElement|HTMLInputElement]]</code>
*<code>[[dom/HTMLTextAreaElement|HTMLTextAreaElement]]</code>
*<code>[[html/attributes/size (control)|size]]</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}