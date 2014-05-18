{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|[[css/properties/transform|Transform]] function for a 2d translation which moves an element on the x-axis by the given value.}}
{{CSS_Function
|Content====Syntax===
'''translateX ( <tranlation-value> )'''

===Parameters===
'''translation-value'''

Value for the translation across the x-axis. Can be a length value or a percentage value.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The example shows three div elements, that are transformed individually with the translateX() function.

# The translation of the first element moves it 10 pixels to the right along the x-axis.
# You can also provide a negative value. In this case, element-2 is moved 20 pixels to the left, in the negative direction on the x-axis.
# Using a percentage value of 50 percent moves element-3 in x-direction by a value which matches 50 percent of the element-3's width. In this case element-3 has a 100 pixel width, so it is moved 50 pixels to the right.
|Code=.element-1 {
	transform: translateX(10px);
}

.element-2 {
	transform: translateX(-20px);
}

.element-3 {
	transform: translateX(50%);
}
|LiveURL=http://codepen.io/Fischaela/pen/dHgbL
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
|Manual_sections====Related pages (MSDN)===
* [http://go.microsoft.com/fwlink/p/?LinkID{{=}}223145 CSS Transforms Module, Level 3], Section 13.1
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