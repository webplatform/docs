{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|An animation timing function that describes a progression of movement as a cubic-bezier curve.}}
{{CSS_Function
|Content=

____



A timing function, based on a cubic-bezier curve, that takes four parameters. The four values specify the x and y-coordinates as (x1, y1, x2, y2) of the P1 and P2 points of the curve, respectively.

'''Note'''  For properties other than opacity and color, the cubic-bezier curve function accepts y-coordinates outside the standard range of [0, 1]. This allows the ability to specify "elastic" effects for properties such as length and width, as shown in the following image.
[[Image:msTransition-ease-in-out-elastic-cubic.png]]


ease: This function is equivalent to
'''cubic-bezier(0.25,0.1,0.25,1)'''. [[Image:msTransition-ease-cubic.png]]

linear A timing function, based on a cubic-bezier curve, that has a
consistent speed from start to end. This function is equivalent to
'''cubic-bezier(0,0,1,1)'''. [[Image:msTransition-linear-cubic.png]]

ease-in A timing function, based on a cubic-bezier curve, that
gradually increases in speed at the start. This function is equivalent
to
'''cubic-bezier(0.42,0,1,1)'''. [[Image:msTransition-ease-in-cubic.png]]

ease-out
A timing function, based on a cubic-bezier curve, that  gradually decreases in speed at the end. This function is equivalent to '''cubic-bezier(0,0,0.58,1)'''. [[Image:msTransition-ease-out-cubic.png]]

ease-in-out A timing function, based on a cubic-bezier curve, that
gradually increases in speed at the start and then gradually decreases
in speed at the end. This function is equivalent to
'''cubic-bezier(0.42,0,0.58,1)'''. [[Image:msTransition-ease-in-out-cubic.png]]




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