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
|Description=This example shows a simple flood filter that is green colored and has an opacity of 50%.

The image will look like this.
|Code=<syntaxhighlight lang="xml">
<!DOCTYPE HTML>
<html>
    <head></head>
    <body>
        <svg width="400" height="400">
            <defs>
               <filter id="MyFilter" filterUnits="userSpaceOnUse" x="0" y="0"  width="400" height="400">
                  <feFlood x="100" y="100" width="100" height="100"
                    flood-color="green" flood-opacity="0.5"/>
               </filter>
            </defs>
            <use filter="url(#MyFilter)" x='0' y='0'/>
            </svg>
    </body>
</html>
</syntaxhighlight>
}}
}}
{{Notes_Section
|Notes====Remarks===

The purpose of this filter is to provide a rectangular area that can be part of a larger filter chain. If you do not supply a color or opacity, the default values will be used. You can supply the [[svg/properties/x|'''x''']], [[svg/properties/y|'''y''']], [[svg/properties/width|'''width''']], and [[svg/properties/height|'''height''']] values, but if you do not, they will be defined by the general filter region.
|Import_Notes====Syntax===

===Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}226062 Scalable Vector Graphics: Filter Effects], Section 15.25.18

===Members===

The '''SVGFEFloodElement''' object has these properties:

*[[svg/properties/height|'''height''']]: Gets or sets  the height of an element.
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