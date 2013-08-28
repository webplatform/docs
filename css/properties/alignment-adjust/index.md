{{Page_Title|alignment-adjust}}
{{Flags
|High-level issues=Stub
|Content=Incomplete, Examples Needed
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The <code>alignment-adjust</code> property allows more precise alignment of elements, such as graphics, that do not have a baseline-table or lack the desired baseline in their baseline-table. With the <code>alignment-adjust</code> property, the position of the baseline identified by the <code>alignment-adjust</code> can be explicitly determined. It also determines precisely the alignment point for each glyph within a textual element. The user agent should use heuristics to determine the position of a non existing baseline for a given element.}}
{{CSS Property
|Initial value=auto
|Applies to=inline-level elements
|Inherited=No
|Media=visual
|Computed value=see text
|Animatable=No
|CSS percentages=refers to the 'line-height' of the element
|Values={{CSS Property Value
|Data Type=baseline
|Description=The alignment point is at the intersection of the start-edge of the element and the dominant-baseline of the element.
}}{{CSS Property Value
|Data Type=before-edge
|Description=The alignment point is at the intersection of the start-edge of the element and the before-edge of the extended inline box of the element. This may include or not the line-height of the element, depending on the line-stacking-strategy.
}}{{CSS Property Value
|Data Type=text-before-edge
|Description=The alignment point is at the intersection of the start-edge of the element and the 'text-before-edge' baseline of the element.
}}{{CSS Property Value
|Data Type=central
|Description=The alignment point is at the intersection of the start-edge of the element and the 'central' baseline of the element.
}}{{CSS Property Value
|Data Type=middle
|Description=The alignment point is at the intersection of the start-edge of the element and the 'middle' baseline of the element.
}}{{CSS Property Value
|Data Type=after-edge
|Description=The alignment point is at the intersection of the start-edge of the element and the after-edge of the extended inline box of the element. This may include or not the line-height of the element, depending on the line-stacking-strategy.
}}{{CSS Property Value
|Data Type=text-after-edge
|Description=The alignment point is at the intersection of the start-edge of the element and the 'text-after-edge' baseline of the element.
}}{{CSS Property Value
|Data Type=ideographic
|Description=The alignment point is at the intersection of the start-edge of the element and the 'ideographic' baseline of the element.
}}{{CSS Property Value
|Data Type=alphabetic
|Description=The alignment point is at the intersection of the start-edge of the element and the 'alphabetic' baseline of the element.
}}{{CSS Property Value
|Data Type=hanging
|Description=The alignment point is at the intersection of the start-edge of the element and the 'hanging' baseline of the element.
}}{{CSS Property Value
|Data Type=mathematical
|Description=The alignment point is at the intersection of the start-edge of the element and the 'mathematical' baseline of the element.
}}{{CSS Property Value
|Data Type=<percentage>
|Description=The computed value of the property is this percentage multiplied by the computed 'line-height' of the element. The alignment point is on the start-edge of the inline box. Its position along the start-edge relative to the intersection of the dominant-baseline and the start-edge is offset by the computed value. The offset is opposite to the shift-direction (positive value) or in the shift-direction (negative value). A value of '0%' makes the dominant-baseline the alignment point.
}}{{CSS Property Value
|Data Type=<length>
|Description=The alignment-point is on the start-edge of the inline box. Its position along the start-edge relative to the intersection of the dominant-baseline and the start-edge is offset by the <length> value. The offset is opposite to the shift-direction (positive value) or in the shift-direction (negative value). A value of '0cm' makes the dominant-baseline the alignment point.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|LiveURL=https://gist.github.com/6363838/2b75af2b68fe30f99c245e7b9e791b4bbad4b1a9
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
{{See_Also_Section}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}