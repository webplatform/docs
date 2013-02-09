{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|An input field for setting a number value that falls in a given range.}}
{{Markup_Element
|DOM_interface=dom/HTMLInputElement
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
If the range control isn’t supported in a browser, it will display the value as a normal text field.
'''Note'''  For code samples, see [http://go.microsoft.com/fwlink/p/?LinkID{{=}}251128 Form controls part 1] and [http://go.microsoft.com/fwlink/p/?LinkID{{=}}251131 Form controls part 2: validation] on the Windows Internet Explorer sample site.
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 4.10.7.1.14


===Members===
The '''input type{{=}}range''' object has these types of members:
*[#properties Properties]


====Properties====
The '''input type{{=}}range''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[html/attributes/max (HTMLInputElement)|'''max''']]
|Defines the maximum acceptable value for an input element with type{{=}}"number".
|-
|[[html/attributes/min|'''min''']]
|Defines the minimum acceptable value for an input element with type{{=}}"number".
|-
|[[html/attributes/step|'''step''']]
|Defines an increment or jump between values that you want to allow the user to enter.
|-
|[[html/attributes/type|'''type''']]
|Retrieves or initially sets  the type of '''input''' control represented by the object.
|-
|[[html/attributes/value (input elements)|'''value''']]
|Sets or retrieves the displayed value for the control object.  This value is returned to the server when the control object is submitted.
|}
 
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=5.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=9.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=2.1
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=7.0
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=18
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=No
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=10
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=10
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=5.0
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=10
|Note=recognises the type and validates properly, but as per spec it does not show a UI
}}{{Compatibility Notes Row
|Browser=Chrome
|Version=5.0
|Note=shows a UI, although this is not a requirement of the spec
}}
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>Reference</code>
*<code>input</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}