{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs summary, spec reference, standardization status
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Markup_Element
|DOM_interface=svg/objects/SVGElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example shows a simple text element and two morphology filters applied to the same text. The first filter thins the text with an [[svg/properties/operator|'''operator''']] value of '''erode''' and  a '''radius'''  value of   1. The second filter thickens the text with an '''operator''' value of '''dilate''' and  and '''radius''' value of   1.2.

The image will look like this.
|Code=<syntaxhighlight lang="xml">
<!DOCTYPE HTML>
<html>
    <head></head>
    <body>
        <svg width="400" height="400">
            <defs>
                <filter id="MyFilter1" filterUnits="userSpaceOnUse" x="50" y="50" width="300" height="300">
                    <feMorphology operator="erode" radius="1"  />
                </filter>
                <filter id="MyFilter2" filterUnits="userSpaceOnUse" x="50" y="50" width="300" height="300">
                    <feMorphology operator="dilate" radius="1.2"  />
                </filter>
            </defs>
            <g font-family="Verdana" font-size="36" stroke="black" stroke-width="2">
                <text x="50" y="50">
                    Unfiltered
                </text>
                <text x="50" y="150" filter="url(#MyFilter1)">
                    Erode
                </text>
                <text x="50" y="250" filter="url(#MyFilter2)">
                    Dilate
                </text>
            </g>
        </svg>
    </body>
</html>
</syntaxhighlight>
}}
}}
{{Notes_Section
|Notes====Remarks===

You can specify thickness or thinness by using the [[svg/properties/operator|'''operator''']] property.

You can specify how much you what to thicken or thin by using the   '''radius''', [[svg/properties/radiusX|'''radiusX''']], and [[svg/properties/radiusY|'''radiusY''']]   properties.
|Import_Notes====Syntax===

===Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}226062 Scalable Vector Graphics: Filter Effects], Section 15.25.23

===Members===

The '''SVGFEMorphologyElement''' object has these properties:

*[[svg/properties/height|'''height''']]: Gets or sets  the height of an element.
*[[svg/properties/in1|'''in1''']]: Identifies input for the given filter primitive.
*[[svg/properties/operator|'''operator''']]: Specifies the operation of whether to thin or thicken.
*[[svg/properties/radiusX|'''radiusX''']]: Specifies the thickening or thinning you want to apply in the X direction.
*[[svg/properties/radiusY|'''radiusY''']]: Specifies the thickening or thinning you want to apply in the Y direction.
*[[svg/properties/result|'''result''']]: Provides a reference for the output result of a filter.
*[[svg/properties/width|'''width''']]: Defines the width of an element.
*[[svg/properties/x|'''x''']]: Gets or sets the x-coordinate value.
*[[svg/properties/y|'''y''']]: Gets or sets the y-coordinate value.
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
|Topic_clusters=Filters
}}
{{Topics|SVG}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}