{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Creates a hit region.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=options
|Data type=Object
|Description=This parameter is of type ''HitRegionOptions''. It can have following members:
* '''id''' ( default empty string ) Used as reference for the HitRegion ( e.g. in [[dom/MouseEvent|MouseEvents]] )
* '''control''' ( default null ) An element ( descendant of the canvas ) to which the event is routed
|Optional=No
}}
|Method_applies_to=apis/canvas/CanvasRenderingContext2D
|Example_object_name=context
|Return_value_name=hitRegion
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=simple click detection
|Code=var canvas = document.getElementById( "mycanvas" );
var ctx = canvas.getContext( "2d" );
ctx.fillStyle = "lime";
ctx.beginPath( );
ctx.rect( 10, 10, 100, 100 );
ctx.fill( );
try {
    ctx.addHitRegion( {"id": "limeRectangle" } );
} catch( e ) {
    alert( "your browser does not support hit regions" );
}
canvas.onclick = function( e ) {
    if( e.region ) {
        alert( "clicked on: " + e.region );
    }
};
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C HTML Canvas 2D Specification
|URL=http://www.w3.org/TR/2012/CR-2dcontext-20121217/
|Status=W3C Candidate Recommendation
}}
}}
{{Notes_Section
|Notes=A ''hit region'' is an arbitrary rectangular area on the canvas that responds to user events, with the goal of simplifying event detection.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C HTML Canvas 2D Specification
|URL=http://www.w3.org/TR/2012/CR-2dcontext-20121217/#hit-regions
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
|Firefox_supported=Yes
|Firefox_version=15.0
|Firefox_prefixed_supported=Unknown
|Internet_explorer_supported=No
|Internet_explorer_prefixed_supported=Unknown
|Opera_supported=Yes
|Opera_version=12.1
|Opera_prefixed_supported=Unknown
|Safari_supported=Yes
|Safari_version=5.1
|Safari_prefixed_supported=Unknown
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=2.1
|Android_prefixed_supported=Unknown
|Blackberry_supported=Yes
|Blackberry_version=7.0
|Blackberry_prefixed_supported=Unknown
|Chrome_mobile_supported=Unknown
|Chrome_mobile_prefixed_supported=Unknown
|Firefox_mobile_supported=Unknown
|Firefox_mobile_prefixed_supported=Unknown
|IE_mobile_supported=Unknown
|IE_mobile_prefixed_supported=Unknown
|Opera_mobile_supported=Unknown
|Opera_mobile_prefixed_supported=Unknown
|Opera_mini_supported=Yes
|Opera_mini_version=5.0-7.0 (partial)
|Opera_mini_prefixed_supported=Unknown
|Safari_mobile_supported=Yes
|Safari_mobile_version=3.2
|Safari_mobile_prefixed_supported=Unknown
}}
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|API, Canvas}}
{{External_Attribution
|Is_CC-BY-SA=No
}}