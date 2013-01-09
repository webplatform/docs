{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Specifies each pixel within a canvas's rectangular selection, via the [[apis/canvas/ImageData|ImageData]] object's [[apis/canvas/ImageData/data|data]] property. The array uses four elements to represent each pixel's red, green, blue, and alpha channels. See Notes.}}
{{API_Object}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes=A Canvas Pixel ArrayBuffer is not, strictly speaking, an object of the canvas API. It is a regular ArrayBuffer object (see [http://www.khronos.org/registry/typedarray/specs/latest/#5 Typed Array Specification, ArrayBuffer Type]) whose data is represented in left-to-right, top-to-bottom order, starting with the top left, with each pixel's red, green, blue, and alpha components being given in that order for each pixel. Each component of each device pixel represented in this array must be in the range 0..255, representing the 8 bit value for that component. The components must be assigned consecutive indices starting with 0 for the top left pixel's red component.
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