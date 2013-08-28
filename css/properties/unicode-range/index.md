{{Page_Title|unicode-range}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|<code>unicode-range</code> allows you to set a specific range of characters to be downloaded from a font (embedded using <code>@font-face</code>) and made available for use on the current page.}}
{{CSS Property
|Initial value=U+0-10FFFF
|Applies to=The <code>@font-face</code> block the property is included inside.
|Inherited=No
|Media=visual
|Computed value=Same as the inputted value
|Animatable=No
|CSS object model property=unicodeRange
|Values={{CSS Property Value
|Data Type=single codepoint
|Description=A single unicode character codepoint, for example <code>unicode-range: U+26</code>.
}}{{CSS Property Value
|Data Type=codepoint range
|Description=A range of unicode codepoints. So for example, <code>unicode-range: U+0025-00FF</code> means "include all characters in the range U+0025 to U+00FF."
}}{{CSS Property Value
|Data Type=wildcard range
|Description=You can specify wildcard characters using the "?" character, so for example <code>unicode-range: U+4??</code> would mean "include all characters in the range U+400 to U+4FF."
}}{{CSS Property Value
|Data Type=multiple value declarations
|Description=You can specify multiple single codepoints and/or codepoint groups, delimiting them using commas. For example, <code>unicode-range: U+00-FF, U+980-9FF</code>.
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}