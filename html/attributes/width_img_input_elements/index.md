{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Deletion Candidate
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example sets the width of the image to 20 pixels regardless of the original size of the image.
|Code=&lt;IMG SRC{{=}}"large.png" WIDTH{{=}}"20"&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
If you specify the '''width''' property of an '''img''', but not the [[html/attributes/height|'''height''']] property, the resulting height of the '''img''' is sized proportionally to the specified '''width''' property and the actual height, in pixels, of the source image file. Consider the following example:
{| class="wikitable"
|-
|Dimensions of image in source file (pixels):
|100 X 50 (W X H)
|-
|Specified image width:
|2in
|-
|Specified image height:
|not specified
|-
|Resulting image width:
|2in
|-
|Resulting image height:
|1in ((50/100) * 2 inches)
|}
 
If you specify the '''width''' property of an '''img''', and the height and width of the image in the source file are identical, the height of the image matches the width.
If you specify the [[html/attributes/height|'''height''']] property and the '''width''' property of an '''img''', the resulting image dimensions match the height and width specified.
When scripting the [[css/cssom/properties/pixelHeight|'''pixelHeight''']] or [[css/cssom/properties/posHeight|'''posHeight''']] property to numerically manipulate the height value.
If dynamic changes are intended for the height and width, the original values should be set through style (for example,  "style{{=}}''height:200px; width:200px'') rather than through the height and width attributes.
Although you can specify the width as a percentage, this property always retrieves the width in pixels.
This property is an integer value. Although an HTML author can specify the width as a percentage, this property always specifies the width in pixels in C++.
If you specify the '''width''' property of an '''img''', but not the [[html/attributes/height|'''height''']] property, the resulting height of the '''img''' is sized proportionally to the specified '''width''' property and the actual height, in pixels, of the source image file. Consider the following example:
{| class="wikitable"
|-
|Dimensions of image in source file (pixels):
|100 X 50 (W X H)
|-
|Specified image width:
|2in
|-
|Specified image height:
|not specified
|-
|Resulting image width:
|2in
|-
|Resulting image height:
|1in ((50/100) * 2 inches)
|}
 
If you specify the '''width''' property of an '''img''', and the height and width of the image in the source file are identical, the height of the image matches the width.
If you specify the [[html/attributes/height|'''height''']] property and the '''width''' property of an '''img''', the resulting image dimensions match the height and width specified.
|Import_Notes====Syntax===
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
|Manual_sections====Related pages (MSDN)===
*<code>img</code>
*<code>input type{{=}}button</code>
*<code>input type{{=}}checkbox</code>
*<code>input type{{=}}file</code>
*<code>input type{{=}}image</code>
*<code>input type{{=}}password</code>
*<code>input type{{=}}radio</code>
*<code>input type{{=}}reset</code>
*<code>input type{{=}}submit</code>
*<code>input type{{=}}text</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}