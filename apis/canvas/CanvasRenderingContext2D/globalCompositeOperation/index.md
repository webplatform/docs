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