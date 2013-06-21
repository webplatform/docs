{{Page_Title}}
{{Flags
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Shapes define arbitrary geometric contours around which inline content flows. The shape-outside property defines the float area for a float.}}
{{CSS Property
|Initial value=auto
|Applies to=floats
|Inherited=No
|Media=visual
|Computed value=computed lengths for <basic-shape>, the absolute URI for <uri>, otherwise as specified
|Animatable=No
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=auto
|Description=The float area uses the margin box as normal.
}}{{CSS Property Value
|Data Type=<basic-shape>
|Description=The shape is computed based on the values of one of ‘rectangle’, ‘inset-rectangle’, ‘circle’, ‘ellipse’ or ‘polygon’.
}}{{CSS Property Value
|Data Type=<uri>
|Description=If the <uri> references an image, which is CORS-same-origin, the shape is extracted and computed based on the alpha channel of the specified image. If the <uri> does not reference an image or if it references an image which is not CORS-same-origin, the effect is as if the value ‘auto’ had been specified.
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=Shapes are declared with the ‘shape-outside’ property, with possible modifications from the ‘shape-margin’ property. The shape defined by the ‘shape-outside’ and ‘shape-margin’ properties changes the geometry of a float element's float area.
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
{{See_Also_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}