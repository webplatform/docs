{{Page_Title|Smarter SVG: shapes}}
{{Flags
|High-level issues=Stub
|Editorial notes=[new content from Sierra to reframe SVG]
}}
{{Byline}}
{{Summary_Section|This guide introduces SVG's basic graphic primitives, from simple lines and shapes to complex polygons and paths.}}
{{Tutorial
|Content=__CONTENT__

==Including SVG==

* embed/link
* style via CSS

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
* marker

==More stroke options==

* stroke-linecap
* stroke-linejoin
* stroke-miterlimit (if linejoin:miter)
* stroke-dasharray
* stroke-dashoffset

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

* z=closepath

 8 Paths
    8.1 Introduction
    8.2 The 'path' element
    8.3 Path data
        8.3.1 General information about path data
        8.3.2 The "moveto" commands
        8.3.3 The "closepath" command
        8.3.4 The "lineto" commands
        8.3.5 The curve commands
        8.3.6 The cubic Bézier curve commands
        8.3.7 The quadratic Bézier curve commands
        8.3.8 The elliptical arc curve commands
        8.3.9 The grammar for path data
    8.4 Distance along a path
    8.5 DOM interfaces
        8.5.1 Interface SVGPathSeg
        8.5.2 Interface SVGPathSegClosePath
        8.5.3 Interface SVGPathSegMovetoAbs
        8.5.4 Interface SVGPathSegMovetoRel
        8.5.5 Interface SVGPathSegLinetoAbs
        8.5.6 Interface SVGPathSegLinetoRel
        8.5.7 Interface SVGPathSegCurvetoCubicAbs
        8.5.8 Interface SVGPathSegCurvetoCubicRel
        8.5.9 Interface SVGPathSegCurvetoQuadraticAbs
        8.5.10 Interface SVGPathSegCurvetoQuadraticRel
        8.5.11 Interface SVGPathSegArcAbs
        8.5.12 Interface SVGPathSegArcRel
        8.5.13 Interface SVGPathSegLinetoHorizontalAbs
        8.5.14 Interface SVGPathSegLinetoHorizontalRel
        8.5.15 Interface SVGPathSegLinetoVerticalAbs
        8.5.16 Interface SVGPathSegLinetoVerticalRel
        8.5.17 Interface SVGPathSegCurvetoCubicSmoothAbs
        8.5.18 Interface SVGPathSegCurvetoCubicSmoothRel
        8.5.19 Interface SVGPathSegCurvetoQuadraticSmoothAbs
        8.5.20 Interface SVGPathSegCurvetoQuadraticSmoothRel
        8.5.21 Interface SVGPathSegList
        8.5.22 Interface SVGAnimatedPathData
        8.5.23 Interface SVGPathElement

 9 Basic Shapes
    9.1 Introduction
    9.2 The 'rect' element
    9.3 The 'circle' element
    9.4 The 'ellipse' element
    9.5 The 'line' element
    9.6 The 'polyline' element
    9.7 The 'polygon' element
        9.7.1 The grammar for points specifications in 'polyline' and 'polygon' elements
    9.8 DOM interfaces
        9.8.1 Interface SVGRectElement
        9.8.2 Interface SVGCircleElement
        9.8.3 Interface SVGEllipseElement
        9.8.4 Interface SVGLineElement
        9.8.5 Interface SVGAnimatedPoints
        9.8.6 Interface SVGPolylineElement
        9.8.7 Interface SVGPolygonElement

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