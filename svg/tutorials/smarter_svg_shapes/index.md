{{Page_Title|Smarter SVG: The Basics}}
{{Flags
|High-level issues=Stub
|Editorial notes=[new content from Sierra to reframe SVG]
}}
{{Byline}}
{{Summary_Section|___SUMMARY__}}
{{Tutorial
|Content=__CONTENT__

==Simple shapes==

* rect
** x y
* circle
** cx cy r
* ellipse
** rx ry

==Fill and stroke==

* fill
* stroke
* stroke-width
* fill-opacity
* stroke-opacity

==Lines and polygons==

* line
** x1 y1 x2 y2
* polyline
** points
* polygon

==More stroke options==

* stroke-linecap
* stroke-linejoin
* stroke-miterlimit (if linejoin:miter)
* stroke-dasharray

==Paths==

* path d attr
* m=moveto
* l=lineto
* h=line horiz to x
* v=line vertical to y
* c=cubic bezier to x,y with 2 x,y controls
* s=cubic bezier alternative to above, but dupe control
* q=quadratic bezier, to x,y dest w/1 x,y control
* t=quadratic bezier alternative to above, but dupe control
* a=elliptical arc to x,y; A rx,ry x-axis-rotation large-arc?,sweep? x,y (Ex: A 100,40 30 0,0 20,20)

}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|SVG}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}