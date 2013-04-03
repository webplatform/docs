{{Page_Title}}
{{Flags
|High-level issues=Unreviewed Import, Needs Review
|Content=Incomplete, Not Neutral, Grammar/Spelling, Cleanup, Compatibility Incomplete, Examples Needed, Needs Summary
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|This property specifies inward offsets from the top, right, bottom, and left edges of the mask image, dividing it into nine regions: four corners, four edges and a middle. The middle image part is discarded (treated as fully transparent black) unless the ‘fill’ keyword is present. 

When four values are specified, they set the offsets on the top, right, bottom and left sides in that order. If the left is missing, it is the same as the right; if the bottom is missing, it is the same as the top; if the right is missing, it is the same as the top.
}}
{{CSS Property
|Inherited=No
|Animatable=No
|Values={{CSS Property Value
|Data Type=length
|Description=all <length>s made absolute, otherwise as specified
}}{{CSS Property Value
|Data Type=percentage
|Description=Percentages refer to the size of the mask box image area: the width of the area for horizontal offsets, the height for vertical offsets. 
}}{{CSS Property Value
|Data Type=number
|Description=Numbers represent multiples of the corresponding computed ‘border-width’.
}}{{CSS Property Value
|Data Type=auto
|Description=If ‘auto’ is specified then the mask box image width is the intrinsic width or height (whichever is applicable) of the corresponding image slice (see ‘mask-box-image-slice’). If the image does not have the required intrinsic dimension then the corresponding ‘border-width’ is used instead. 
}}{{CSS Property Value
|Data Type=fill
|Description=The ‘fill’ keyword, if present, causes the middle part of the mask image to be preserved. (By default it is discarded, i.e., treated as transparent black.) 
}}
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
{{See_Also_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}