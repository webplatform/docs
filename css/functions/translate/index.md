{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|A 2d transition which sets the position of an element to a new one, described by two vectors (x, y). The y value is optional.}}
{{CSS_Function
|Content===Syntax==
* '''translate ( translation-value-x )'''
* '''translate ( translation-value-x, translate-value-y )'''

==Values==
'''translation-value-x'''

''Value for the translation across the x-axis. Can be a [[css/data_types/length|length]] value or a [[css/data_types/percentage|percentage]] value. Value for the y-axis translation is assumed to be zero.''

'''translation-value-x, translate-value-y'''

''First value describes the translation across the x-axis, the second across the y-axis. Values can be a [[css/data_types/length|length]] or a [[css/data_types/percentage|percentage]] value.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following code snippet is an example of the '''translate''' function in use. When applied to a square blue [[html/elements/div|'''div''']] element, it has the effect illustrated in the image. (The light-blue square indicates the original position of the transformed element.)
|Code=div {    
  transform: translate(47px, -38px);
}
}}
}}
{{Notes_Section
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkID{{=}}223145 CSS Transforms Module, Level 3], Section 13.1


===Requirements===
{| class="wikitable"
|}
}}
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
{{See_Also_Section
|Topic_clusters=Transforms
|Manual_sections====Related pages (MSDN)===
*<code>Transform Functions</code>
*<code>[http://go.microsoft.com/fwlink/p/?LinkId{{=}}256246 Mathematical Description of Transform Functions]</code>
*<code>[http://go.microsoft.com/fwlink/?LinkID{{=}}240163 Hands On: 2D Transforms]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}