{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Depending on how it is called, returns either an '''ImageData''' object with the given ''sw, sh'' dimensions or an '''ImageData''' object with the same dimensions as the ''imagedata'' argument. See Notes.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=sw
|Data type=Number
|Description=The width of the new object, in CSS pixels.
|Optional=No
}}{{Method Parameter
|Name=sh
|Data type=Number
|Description=The height of the new object, in CSS pixels.
|Optional=No
}}{{Method Parameter
|Name=imagedata
|Data type=Object
|Description=An '''imagedata''' object of the desired width and height.
|Optional=No
}}
|Method_applies_to=apis/canvas/CanvasRenderingContext2D
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=An '''ImageData''' object.
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes=When this method is invoked with two arguments, ''sw'' and ''sh'', it returns an '''ImageData''' object representing a rectangle with a width in CSS pixels equal to the absolute magnitude of ''sw'' and a height in CSS pixels equal to the absolute magnitude of ''sh''. When invoked with a single ''imagedata'' argument, it returns an '''ImageData''' object representing a rectangle with the same dimensions as the '''ImageData''' object passed as the argument. The object returned is filled with transparent black.
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