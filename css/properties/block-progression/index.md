{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section}}
{{CSS Property
|Applies to=All elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=tb
|Description=Default. Top-to-bottom block flow. Layout is horizontal.
}}{{CSS Property Value
|Data Type=rl
|Description=Right-to-left block flow. Layout is vertical.
}}{{CSS Property Value
|Data Type=bt
|Description=Bottom-to-top block flow. Layout is horizontal.
}}{{CSS Property Value
|Data Type=lr
|Description=Left-to-right block flow. Layout is vertical.
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
In vertical layout, text lines are rotated 90° clockwise. Images are not rotated, but tables are. Box layout in vertical orientations is exactly analogous to layout in the horizontal orientation: width, height, top, bottom, right, and left do not rotate with the text.
Only one block progression is active at a time; these values cannot be combined. See [[css/properties/writing-mode|'''-ms-writing-mode''']] for additive block progression values.
This property is based on the block-progression property of the [http://go.microsoft.com/fwlink/p/?linkid{{=}}203505 CSS3 Text Layout] module.
|Import_Notes====Syntax===
<code>'''-ms-block-progression: '''tb '''{{!}}''' rl '''{{!}}''' bt '''{{!}}''' lr</code>
===Standards information===
There are no standards that apply here.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Text
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[css/properties/direction|direction]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}