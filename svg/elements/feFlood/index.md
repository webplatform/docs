{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Markup_Element
|DOM_interface=svg/objects/SVGElement
}}
{{Topics|SVG}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example shows a simple flood filter that is green colored and has an opacity of 50%.

The image will look like this.
|LiveURL=
|Code=
&lt;!DOCTYPE HTML&gt;
&lt;html&gt;
    
    &lt;head&gt;
    &lt;/head&gt;
    
    &lt;body&gt;
        &lt;svg width{{=}}"400" height{{=}}"400"&gt;
        
            &lt;defs&gt;
               &lt;filter id{{=}}"MyFilter" filterUnits{{=}}"userSpaceOnUse" 
                 x{{=}}"0" y{{=}}"0"  width{{=}}"400" height{{=}}"400"&gt;
                  &lt;feFlood x{{=}}"100" y{{=}}"100" width{{=}}"100" height{{=}}"100" 
                    flood-color{{=}}"green" flood-opacity{{=}}"0.5"/&gt;
               &lt;/filter&gt;
            &lt;/defs&gt;
            &lt;use filter{{=}}"url(#MyFilter)" x{{=}}'0' y{{=}}'0'/&gt;				
            &lt;/svg&gt;
    &lt;/body&gt;

&lt;/html&gt;

}}}}
{{Notes_Section
|Notes=
===Remarks===
The purpose of this filter is to provide a rectangular area that can be part of a larger filter chain. If you do not supply a color or opacity, the default values will be used. You can supply the [[svg/properties/x|'''x''']], [[svg/properties/y|'''y''']], [[svg/properties/width|'''width''']], and [[svg/properties/height|'''height''']] values, but if you do not, they will be defined by the general filter region.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}226062 Scalable Vector Graphics: Filter Effects], Section 15.25.18


===Members===
The '''SVGFEFloodElement''' object has these types of members:
*[#properties Properties]


====Properties====
The '''SVGFEFloodElement''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[svg/properties/height|'''height''']]
|Gets or sets  the height of an element.
|-
|[[svg/properties/result|'''result''']]
|Provides a reference for the output result of a filter.
|-
|[[svg/properties/width|'''width''']]
|Defines the width of an element.
|-
|[[svg/properties/x|'''x''']]
|Gets or sets the x-coordinate value.
|-
|[[svg/properties/y|'''y''']]
|Gets or sets the y-coordinate value.
|}
 

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}