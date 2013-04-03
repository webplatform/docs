{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The mask image is drawn inside an area called the mask box image area. This is an area whose boundaries by default correspond to the mask box, see ‘mask-box-image-outset’. 

The four values of ‘mask-box-image-width’ specify offsets that are used to divide the mask box image area into nine parts. They represent inward distances from the the top, right, bottom, and left sides of the area, respectively. If the left width is missing, it is the same as the right; if the bottom is missing, it is the same as the top; if the right is missing, it is the same as the top.
}}
{{CSS Property
|Inherited=No
|Animatable=No
|Values={{CSS Property Value
|Data Type=length
}}{{CSS Property Value
|Data Type=percentage
|Description=Percentages refer to the size of the mask box image area: the width of the area for horizontal offsets, the height for vertical offsets. 
}}{{CSS Property Value
|Data Type=number
|Description=Numbers represent multiples of the corresponding computed ‘border-width’. 
}}{{CSS Property Value
|Data Type=auto
|Description=If ‘auto’ is specified then the mask box image width is the intrinsic width or height (whichever is applicable) of the corresponding image slice (see ‘mask-box-image-slice’). If the image does not have the required intrinsic dimension then the corresponding ‘border-width’ is used instead. 
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