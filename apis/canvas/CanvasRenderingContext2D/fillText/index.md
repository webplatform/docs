{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Renders the given text at the given (x, y) coordinates, ensuring that the text isn't wider than maxWidth (if specified), using the current font, textAlign, and textBaseline values.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=text
|Data type=String
|Description=The text characters to paint on the canvas.
|Optional=No
}}{{Method Parameter
|Name=x
|Data type=Number
|Description=The horizontal coordinate to start painting the text at, relative to the canvas.
|Optional=No
}}{{Method Parameter
|Name=y
|Data type=Number
|Description=The vertical coordinate to start painting the  text, relative to the canvas.
|Optional=No
}}{{Method Parameter
|Name=maxWidth
|Data type=Number
|Description=The maximum possible text width. If the value is less than the  [[apis/canvas/TextMetrics/width|width]] property, the text  is  scaled to fit.
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
{{!}}SecurityError
{{!}}The current font is not of the same origin or domain as the document that owns the canvas element.
{{!}}}
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section}}
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