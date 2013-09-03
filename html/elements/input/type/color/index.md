{{Page_Title}}
{{Flags
|High-level issues=Merge Candidate
|Checked_Out=No
|Editorial notes={{Editorial/Merge_Candidate
|Other=[[html/attributes/type]]
}}
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The '''color''' type of the [[html/elements/input|&lt;input&gt;]] element provides a widget for selecting a color value.}}
{{Markup_Element
|DOM_interface=dom/HTMLInputElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=When viewed using a supporting user agent, the following example shows a field, usually indicating a red color. When clicked, a color picker shows up. Selecting a color would change the indicated color to the chosen color.
|Code=&lt;input type="color" value="#ff0000"/&gt;
}}
}}
{{Notes_Section
|Usage=Use this input type to let the user choose a color using a standard color picker.
|Notes=*Currently, most user agents do not implement this input type. A customized implementation or poly-fill can usually provide a close alternative.
*The value can only express opaque colors, there is no support for an alpha channel/transparency.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=20
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=No
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=11.00
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=No
|Android_version=
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_prefixed_supported=No
|Blackberry_prefixed_version=
|Chrome_mobile_supported=No
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=No
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=No
|IE_mobile_version=
|IE_mobile_prefixed_supported=No
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=6 and later
|Note=For an alternative, non standard implementation, see [[dom/methods/ChooseColorDlg|ChooseColorDlg]].
}}
}}
{{See_Also_Section}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}