{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Specifies the size, zoom factor, and orientation of the viewport.}}
{{CSS_At_Rule
|Content=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=
|Code=@media screen and (max-width:400px) {
    @-ms-viewport{
        width:320px;
        /* the viewport for small devices is set to 320px  */
    }
    @-o-viewport {
        width: device-width;
    }
    @viewport {
        width: device-width;
    }
}
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
You can use the '''@viewport''' rule in tandem with media queries to help optimize your layout. Typically, you nest the '''@viewport''' rule inside the media query, as shown in the following pseudocode snippet:
<code>@media [media query logic here] {
@viewport {
[viewport properties here]
}
[CSS for this layout combination here]
}</code>
|Import_Notes====Syntax===
<code>'''@viewport '''{ ''viewport-properties'' }</code>
===Parameters===
;''viewport-properties'':One or more property declarations, each with a trailing semicolon. Only the following viewport properties are supported.

{{{!}}
! Value
! Meaning
{{!}}-
{{!}}
; '''width'''
{{!}}
Indicates the preferred viewport width used in determining the size of the initial containing block. Can be one of the following values:

; '''auto'''
: The value is calculated based on the display device's normal mode of operation.
; '''device-width'''
: The width of the screen in CSS pixels at a zoom factor of 100%.
; '''device-height'''
: The height of the screen in CSS pixels at a zoom factor of 100%.
; '''length'''
: A positive absolute or relative length.
; '''percentage'''
: A positive percentage value relative to the width or height of the initial viewport at a zoom factor of 100%, for horizontal and vertical lengths respectively.
{{!}}-
{{!}}
; '''height'''
{{!}} Indicates the preferred viewport height used in determining the size of the initial containing block. See '''width''' for a list of possible values.
{{!}}}
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Device Adaptation
|URL=http://www.w3.org/TR/css-device-adapt/#the-viewport-rule
|Status=Working Draft
|Relevant_changes=
}}
}}
{{See_Also_Section
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
{{Editorial/Content_Incomplete}}










{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=width, height support
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Unknown
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Yes
|Internet_explorer_prefixed_version=10
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Yes
|Opera_prefixed_version=11+
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
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
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Yes
|IE_mobile_prefixed_version=10.0
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Yes
|Opera_mobile_prefixed_version=11+
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Unknown
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=10.0
|Note=Partial support. Not all properties are available.
}}
}}