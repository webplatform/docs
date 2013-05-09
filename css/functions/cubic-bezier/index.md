{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|An animation timing function that describes a progression of movement as a cubic-bezier curve.}}
{{CSS_Function
|Content=The function describes a cubic bezier curve starting at 0,0 and ending at 1,1.  It accepts four arguments (x1, y1, x2, y2) that specify coordinates for the two control points that affect the shape of the curve. The following shows standard timing keyword values along with their functional equivalents. The ''x'' axis represents the elapsed time of the animation, and ''y'' represents the progression of movement, so the more the curve points upwards, the faster the animation moves at that point:

<div style="display:inline-block">
[[Image:transitF_linear.png|230px]] <br/>
'''linear''' <br/> '''cubic-bezier(0.0, 0.0, 1.0, 1.0)'''
</div>

<div style="display:inline-block">
[[Image:transitF_ease.png|230px]] <br/>
'''ease''' <br/> '''cubic-bezier(0.25, 0.1, 0.25, 1.0)'''
</div>

<div style="display:inline-block">
[[Image:transitF_easeinout.png|230px]] <br/>
'''ease-in-out''' <br/> '''cubic-bezier(0.42, 0, 0.58, 1.0)'''
</div>

<div style="display:inline-block">
[[Image:transitF_easein.png|230px]] <br/>
'''ease-in''' <br/> '''cubic-bezier(0.42, 0, 1.0, 1.0)'''
</div>

<div style="display:inline-block">
[[Image:transitF_easeout.png|230px]] <br/>
'''ease-out''' <br/> '''cubic-bezier(0, 0, 0.58, 1.0)'''
</div>


'''Note'''  For properties other than opacity and color, the cubic-bezier curve function accepts y-coordinates outside the standard range of [0, 1]. This allows the ability to specify "elastic" effects for properties such as length and width, as shown in the following image.
[[Image:msTransition-ease-in-out-elastic-cubic.png]]



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
{{See_Also_Section
|Topic_clusters=Animation
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}