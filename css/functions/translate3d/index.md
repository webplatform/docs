{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=might be able to merge with regular translate function, with a notation on how the 3D version differs
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|[[css/properties/transform|Transform]] function for a 3d translation which moves an element on x-axis, y-axis and z-axis by the given values.}}
{{CSS_Function
|Content===Syntax==
'''translate3d ( <translation-value-x>, <translation-value-y>, <translation-value-z> )'''

==Parameters==
'''translation-value-x, translation-value-y, translation-value-z'''

''translation-value-x and translation-value-y represent vector values x and y and can be a [[css/data_types/length|length]] or a [[css/data_types/percentage|percentage]] value.''

''translation-value-z is the third vector value and defines the translation in the direction of the z-axis (3rd dimension).'' 
'''Attention:''' ''It can only be a [[css/data_types/length|length]] value, percentage is not supported.''
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The example shows three div elements, that are transformed individually with the translateY() function.

# The translation of the first element moves it 150 pixels to the right along the x-axis.
# The second element is moved 120 pixels down along the positive direction of the y-axis.
# The last translation of element-3 is moving the div 120 pixels in the negative direction of the z-axis. Note that you have to apply a value for the [[css/properties/perspective|perspective]] also, since without it the translation is not visible.
|Code=.element-1 {
	transform: translate3d(150px, 0, 0);
}

.element-2 {
	transform: translate3d(0, 120px, 0);
}

.element-3 {
	transform: perspective(400) translate3d(0, 0, -120px);
}
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
|External_links=* [http://go.microsoft.com/fwlink/p/?LinkID{{=}}223145 CSS Transforms Module, Level 3], Section 13.2
* [http://go.microsoft.com/fwlink/p/?LinkId{{=}}256246 Mathematical Description of Transform Functions]
* [http://go.microsoft.com/fwlink/?LinkId{{=}}227893 Hands On: 3-D Transforms]
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}