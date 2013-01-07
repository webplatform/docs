{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Returns a '''CanvasPattern''' object that uses the given ''image'' and repeats in the direction(s) given by the ''repetition'' argument.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=image
|Data type=DOM Node
|Description=An image, canvas, or video element of the pattern to  use. If the image has no image data, throws an ''InvalidStateError'' exception. If the image is not yet fully decoded, the method returns null.
|Optional=No
}}{{Method Parameter
|Name=repetition
|Data type=any
|Description=The direction of repetition. The allowed values for repetition are:
* "repeat" (both directions; default)
* "repeat-x" (horizontal only)
* "repeat-y" (vertical only)
* "no-repeat" (neither).

If the parameter does not match one of the allowed values, the method throws a ''SyntaxError'' exception. 
|Optional=No
}}
|Method_applies_to=canvas/objects/CanvasRenderingContext2D
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description='''CanvasPattern'''

The pattern object to use as a ''fill style'' together with a ''CanvasRenderingContext2D'' object.
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes=If  the ''repetition''  parameter equals null or an empty string, the method defaults to "repeat".
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