{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|[[css/properties/transform|Transform]] function for a 2d transition which sets the position of an element to a new one, described by two vectors (x, y). The y value is optional.}}
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
|Language=CSS
|Description=The example shows three div elements, that are transformed individually with the translate() function.
# The translation of element-1 visually is making no difference from its origin, because it has twice '''zero''' as translation-values.
# The second translation only provides a '''single translation-value-x''', the second value is set to zero by default here. The div moves 20px to the right.
# For element-3 '''both translation-values''' are set. The div is moved 40px to the right and 80px down.
|Code=.element-1 {
	transform: translate(0, 0);
}

.element-2 {
	transform: translate(20px);
}

.element-3 {
	transform: translate(40px, 80px);
}
|LiveURL=http://codepen.io/Fischaela/pen/Lqmxb
}}
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
{{See_Also_Section
|Topic_clusters=Transforms
|External_links=* [http://go.microsoft.com/fwlink/p/?LinkID{{=}}223145 CSS Transforms Module, Level 3], Section 13.1
* [http://go.microsoft.com/fwlink/p/?LinkId{{=}}256246 Mathematical Description of Transform Functions]
* [http://go.microsoft.com/fwlink/?LinkID{{=}}240163 Hands On: 2D Transforms]
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}