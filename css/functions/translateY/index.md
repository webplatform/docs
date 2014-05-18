{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|[[css/properties/transform|Transform]] function for a 2d translation which moves an element on the y-axis by the given value. Note that the y-axis increases vertically downwards: positive lengths shift the element down, while negative lengths shift it up.}}
{{CSS_Function
|Content===Syntax==
'''translateY( <translation-value> )'''

==Parameters==
'''translation-value'''

''Value for the translation across the y-axis. Can be a [[css/data_types/length|length]]  or a [[css/data_types/percentage|percentage]] value.''
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The example shows three div elements, that are transformed individually with the translateY() function.

# The translation of the first element moves it 10 pixels up along the y-axis.
# You can also provide a negative value. In this case, element-2 is moved 20 pixels to the top, in the negative direction on the y-axis.
# Using a percentage value of 50 percent moves element-3 in positive y-direction by a value which matches 50 percent of the element-3's width. In this case element-3 has a 100 pixel width, so it is moved 50 pixels up.
|Code=.element-1 {
	transform: translateY(10px);
}

.element-2 {
	transform: translateY(-20px);
}

.element-3 {
	transform: translateY(50%);
}
|LiveURL=http://codepen.io/Fischaela/pen/uxgil
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