{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Sets how shapes and images are drawn onto the existing bitmap once they have had globalAlpha and the current transformation matrix applied.}}
{{API_Object_Property
|Property_applies_to=apis/canvas/CanvasRenderingContext2D
|Read_only=No
|Example_object_name=CanvasRenderingContext2D
|Javascript_data_type=String
|Return_value_description=Must be set to a value from the following list. In the descriptions below, the source image, ''A'', is the shape or image being rendered; the destination image, ''B'', is the current state of the bitmap. '''Note:''' Values are case-sensitive.

* "source-atop" - A atop B. Display the source image wherever both images are opaque. Display the destination image wherever the destination image is opaque but the source image is transparent. Display transparency elsewhere.
* "source-in" - A in B. Display the source image wherever both the source image and destination image are opaque. Display transparency elsewhere.
* "source-out" - A out B. Display the source image wherever the source image is opaque and the destination image is transparent. Display transparency elsewhere.
* "source-over" (default) - A over B. Display the source image wherever the source image is opaque. Display the destination image elsewhere.
* "destination-atop" - B atop A. Same as source-atop but using the destination image instead of the source image and vice versa.
* "destination-in" - B in A. Same as source-in but using the destination image instead of the source image and vice versa.
* "destination-out" - B out A. Same as source-out but using the destination image instead of the source image and vice versa.
* "destination-over" - B over A. Same as source-over but using the destination image instead of the source image and vice versa.
* "lighter" - A plus B. Display the sum of the source image and destination image, with color values approaching 255 (100%) as a limit.
* "copy" - A (B is ignored). Display the source image instead of the destination image.
* "xor" - A xor B. Exclusive OR of the source image and destination image.
* ''vendorName-operationName'' - Vendor-specific extensions to the list of composition operators should use this syntax.
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes=You can copy images  directly, or you can apply them depending on the opacity or transparency of the images or by using an XOR operation.
Values are case-sensitive. If you set an unsupported or unrecognized value, ''globalCompositeOperation''  retains the previous value.
|Import_Notes=`
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
|Desktop_rows=
|Mobile_rows=
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