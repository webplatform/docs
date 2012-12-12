{{Page_Title}}
{{Flags
|High-level issues=Stub
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Sets the line dash properties for the stroke.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=sequence
|Data type=Object
|Description=An array of integers that specifies the length of each "on" and "off" segment.
|Optional=No
}}
|Method_applies_to=canvas/objects/CanvasRenderingContext2D
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Creates a dashed line that alternates 15 pixels on and 15 pixels off.
|Code=// Create canvas and get 2D context:
var canvas = document.createElement('canvas');
document.body.appendChild(canvas);
canvas.setAttribute('width', '700');
canvas.setAttribute('height', '700');
var ctx = canvas.getContext('2d');

// Set dash-style, and draw stroke
ctx.setLineDash([15]);
ctx.strokeRect (10,10,100,100);
}}{{Single Example
|Language=JavaScript
|Description=Creates a dashed line that alternates between 15 pixels and 5 pixels off.
|Code=// Create canvas and get 2D context:
var canvas = document.createElement('canvas');
document.body.appendChild(canvas);
canvas.setAttribute('width', '700');
canvas.setAttribute('height', '700');
var ctx = canvas.getContext('2d');

// Set dash-style, and draw stroke
ctx.setLineDash([15, 5]);
ctx.strokeRect (10,10,100,100);
}}
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