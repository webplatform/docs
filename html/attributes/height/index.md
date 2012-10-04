{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Topics|HTML}}
{{Notes_Section
|Notes=
===Remarks===
If the '''height''' property of an '''img''' is specified, but the [[html/attributes/width  (img, input elements)|'''width''']] property is not specified, the resulting width of the '''img''' is sized proportionally according to the specified '''height''' property and the actual width (in pixels) of the image in the source file.
Consider the following:
{| class="wikitable"
|-
|Dimensions of image in source file (pixels):
|100 X 50 (W X H)
|-
|Specified image height:
|2in
|-
|Specified image width:
|not specified
|-
|Resulting image height:
|2in
|-
|Resulting image width:
|4in ((100 / 50) * 2 inches)
|}
 
If you specify the '''height''' property of an '''img''', and the height and width of the image in the source file are identical, the width of the image matches the height.
If you specify the '''height''' property and the [[html/attributes/width  (img, input elements)|'''width''']] property of an '''img''', the resulting image dimensions matches those specified.
Percentage values are based on the height of the parent object.
When scripting the height property, use either the [[css/cssom/properties/pixelHeight|'''pixelHeight''']] or [[css/cssom/properties/posHeight|'''posHeight''']] property to numerically manipulate the height value.
If dynamic changes are intended for the height and width, the original values should be set through style (for example, "style{{=}}''height:200px; width:200px'') rather than through the height and width attributes.
This property specifies the calculated height of the object, in pixels. For table rows and table cells, this property has a range of 0 to 32750 pixels.
If you set the value of the corresponding HTML attribute using a percentage, this property specifies the height, in pixels, represented by that percentage.
The scripting property is read/write for the '''img''' object, but read-only for other objects.
For more information about how to access the dimension and location of objects on the page through the Dynamic HTML (DHTML) Document Object Model (DOM), see Measuring Element Dimension and Location with CSSOM in Internet Explorer 9.
In Microsoft Internet Explorer 5 it is possible to set the '''height''' property, but doing so has no effect on the rendering of the frame.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>embed</code>
*<code>frame</code>
*<code>iframe</code>
*<code>img</code>
*<code>input type{{=}}image</code>
*<code>marquee</code>
*<code>noBR</code>
*<code>object</code>
*<code>[[html/elements/table|table]]</code>
*<code>td</code>
*<code>th</code>
|Topic_clusters=html
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}