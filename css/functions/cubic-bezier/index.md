{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Content=Examples Needed
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

For properties unrelated to opacity and color, the function accepts ''y'' coordinates outside the standard range between 0 and 1. This allows for "elastic" effects in which positions or dimensions may cross over themselves during the course of the progression. The first example below bounces past its start and end points, while the second oscillates more dramatically:

<div style="display:inline-block">
[[Image:transitF_cubicBounce.png|230px]] <br/>
'''cubic-bezier(0.25, -0.5, 0.75, 1.5)'''
</div>

<div style="display:inline-block">
[[Image:transitF_cubicWave.png|230px]] <br/>
'''cubic-bezier(0.5, 2, 0.5, -1)'''
</div>
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=Other
|Description=This sample page demonstrates a sequence of two transitions, whose timing function you can configure.
|LiveURL=http://letmespellitoutforyou.com/samples/transit_timing.html
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
|Topic_clusters=Animation, Transistions
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}