{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Writes data from ImageData structures back to the canvas. If any of the arguments are infinite or NaN, the method must throw a NotSupportedError exception. When the last four arguments are omitted, they must be assumed to have the values 0, 0, the width member of the imagedata structure, and the height member of the imagedata structure, respectively.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=imagedata
|Data type=any
|Description=An ''ImageData'' object with  an image's pixel data.
|Optional=No
}}{{Method Parameter
|Name=dx
|Data type=any
|Description=The x-coordinate, in pixels, of the upper-left corner of the rectangle in relation to the coordinates of the canvas.
|Optional=No
}}{{Method Parameter
|Name=dy
|Data type=any
|Description=The y-coordinate, in pixels, of the upper-left corner of the rectangle in relation to the coordinates of the canvas.
|Optional=No
}}{{Method Parameter
|Name=dirtyX
|Data type=any
|Description=The horizontal (x) value, in CSS pixels, where to place  the image on  the canvas.
|Optional=Yes
}}{{Method Parameter
|Name=dirtyY
|Data type=any
|Description=The vertical (y) value, in CSS pixels, where to place  the image on  the canvas.
|Optional=Yes
}}{{Method Parameter
|Name=dirtyWidth
|Data type=any
|Description=The destination width value, in CSS pixels, to use  to  draw  the image to the canvas.
|Optional=Yes
}}{{Method Parameter
|Name=dirtyHeight
|Data type=any
|Description=The destination height value, in CSS pixels to use  to  draw  the image to  the canvas.
|Optional=Yes
}}
|Method_applies_to=apis/canvas/CanvasRenderingContext2D
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

This method can return one of these values.

{{{!}} class="wikitable"
{{!}}-
!Return code
!Description
{{!}}-
{{!}}S_OK
{{!}}The operation completed successfully.
{{!}}-
{{!}}NotSupportedError
{{!}}One of the parameters is infinite or not a number (NaN).
{{!}}-
{{!}}TypeMismatchError
{{!}}The first parameter is not an CanvasImageData object.
{{!}}-
{{!}}SecurityError
{{!}}The image is not of the same origin or domain as the destination.
{{!}}}

}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes=You can specify an optional rectangle  to show only those pixels. This  "dirty" rectangle refers to a section of pixels to paint.  You can use this option  to  specify areas on an image that might  change  without repainting the complete image.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C HTML Canvas 2D Specification
|URL=http://www.w3.org/TR/2012/CR-2dcontext-20121217/
|Status=W3C Candidate Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=22.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=15.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.1
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=2.1
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=7.0
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_version=5.0-7.0 (partial)
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=3.2
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|Canvas}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}