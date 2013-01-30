{{Page_Title|Smarter SVG: overview and scope}}
{{Flags
|High-level issues=Stub
|Editorial notes=[new content from Sierra to reframe SVG]
}}
{{Byline}}
{{Summary_Section|__SUMMARY__}}
{{Tutorial
|Content=__CONTENT__

==Deploying SVG==

==Adding Styles==

==Grouping Elements==

==The viewport and viewbox==

==Transforms==

 5 Document Structure
    5.1 Defining an SVG document fragment: the 'svg' element
        5.1.1 Overview
        5.1.2 The 'svg' element
    5.2 Grouping: the 'g' element
        5.2.1 Overview
        5.2.2 The 'g' element
    5.3 Defining content for reuse, and the 'defs' element
        5.3.1 Overview
        5.3.2 The 'defs' element
    5.4 The 'desc' and 'title' elements
    5.5 The 'symbol' element
    5.6 The 'use' element
    5.7 The 'image' element
    5.8 Conditional processing
        5.8.1 Conditional processing overview
        5.8.2 The 'switch' element
        5.8.3 The 'requiredFeatures' attribute
        5.8.4 The 'requiredExtensions' attribute
        5.8.5 The 'systemLanguage' attribute
        5.8.6 Applicability of test attributes
    5.9 Specifying whether external resources are required for proper rendering
    5.10 Common attributes
        5.10.1 Attributes common to all elements: 'id' and 'xml:base'
        5.10.2 The 'xml:lang' and 'xml:space' attributes
    5.11 DOM interfaces
        5.11.1 Interface SVGDocument
        5.11.2 Interface SVGSVGElement
        5.11.3 Interface SVGGElement
        5.11.4 Interface SVGDefsElement
        5.11.5 Interface SVGDescElement
        5.11.6 Interface SVGTitleElement
        5.11.7 Interface SVGSymbolElement
        5.11.8 Interface SVGUseElement
        5.11.9 Interface SVGElementInstance
        5.11.10 Interface SVGElementInstanceList
        5.11.11 Interface SVGImageElement
        5.11.12 Interface SVGSwitchElement
        5.11.13 Interface GetSVGDocument

 6 Styling
    6.1 SVG's styling properties
    6.2 Usage scenarios for styling
    6.3 Alternative ways to specify styling properties
    6.4 Specifying properties using the presentation attributes
    6.5 Styling with XSL
    6.6 Styling with CSS
    6.7 Case sensitivity of property names and values
    6.8 Facilities from CSS and XSL used by SVG
    6.9 Referencing external style sheets
    6.10 The 'style' element
    6.11 The 'class' attribute
    6.12 The 'style' attribute
    6.13 Specifying the default style sheet language
    6.14 Property inheritance
    6.15 The scope/range of styles
    6.16 User agent style sheet
    6.17 Aural style sheets
    6.18 DOM interfaces
        6.18.1 Interface SVGStyleElement

 7 Coordinate Systems, Transformations and Units
    7.1 Introduction
    7.2 The initial viewport
    7.3 The initial coordinate system
    7.4 Coordinate system transformations
    7.5 Nested transformations
    7.6 The 'transform' attribute
    7.7 The 'viewBox' attribute
    7.8 The 'preserveAspectRatio' attribute
    7.9 Establishing a new viewport
    7.10 Units
    7.11 Object bounding box units
    7.12 Intrinsic sizing properties of the viewport of SVG content
    7.13 Geographic coordinate systems
    7.14 The 'svg:transform' attribute
    7.15 DOM interfaces
        7.15.1 Interface SVGPoint
        7.15.2 Interface SVGPointList
        7.15.3 Interface SVGMatrix
        7.15.4 Interface SVGTransform
        7.15.5 Interface SVGTransformList
        7.15.6 Interface SVGAnimatedTransformList
        7.15.7 Interface SVGPreserveAspectRatio
        7.15.8 Interface SVGAnimatedPreserveAspectRatio

 21 Metadata
    21.1 Introduction
    21.2 The 'metadata' element
    21.3 An example
    21.4 DOM interfaces
        21.4.1 Interface SVGMetadataElement

 22 Backwards Compatibility

 23 Extensibility
    23.1 Foreign namespaces and private data
    23.2 Embedding foreign object types
    23.3 The 'foreignObject' element
    23.4 An example
    23.5 Adding private elements and attributes to the DTD
    23.6 DOM interfaces
        23.6.1 Interface SVGForeignObjectElement

 1 Introduction
    1.1 About SVG
    1.2 SVG MIME type, file name extension and Macintosh file type
    1.3 SVG Namespace, Public Identifier and System Identifier
    1.4 Compatibility with Other Standards Efforts
    1.5 Terminology
    1.6 Definitions

 2 Concepts
    2.1 Explaining the name: SVG
    2.2 Important SVG concepts
    2.3 Options for using SVG in Web pages

 3 Rendering Model
    3.1 Introduction
    3.2 The painters model
    3.3 Rendering Order
    3.4 How groups are rendered
    3.5 How elements are rendered
    3.6 Types of graphics elements
        3.6.1 Painting shapes and text
        3.6.2 Painting raster images
    3.7 Filtering painted regions
    3.8 Clipping, masking and object opacity
    3.9 Parent Compositing

 4 Basic Data Types and Interfaces
    4.1 Syntax
    4.2 Basic data types
    4.3 Real number precision
    4.4 Recognized color keyword names
    4.5 Basic DOM interfaces
        4.5.1 Interface SVGElement
        4.5.2 Interface SVGAnimatedBoolean
        4.5.3 Interface SVGAnimatedString
        4.5.4 Interface SVGStringList
        4.5.5 Interface SVGAnimatedEnumeration
        4.5.6 Interface SVGAnimatedInteger
        4.5.7 Interface SVGNumber
        4.5.8 Interface SVGAnimatedNumber
        4.5.9 Interface SVGNumberList
        4.5.10 Interface SVGAnimatedNumberList
        4.5.11 Interface SVGLength
        4.5.12 Interface SVGAnimatedLength
        4.5.13 Interface SVGLengthList
        4.5.14 Interface SVGAnimatedLengthList
        4.5.15 Interface SVGAngle
        4.5.16 Interface SVGAnimatedAngle
        4.5.17 Interface SVGColor
        4.5.18 Interface SVGICCColor
        4.5.19 Interface SVGRect
        4.5.20 Interface SVGAnimatedRect
        4.5.21 Interface SVGUnitTypes
        4.5.22 Interface SVGStylable
        4.5.23 Interface SVGLocatable
        4.5.24 Interface SVGTransformable
        4.5.25 Interface SVGTests
        4.5.26 Interface SVGLangSpace
        4.5.27 Interface SVGExternalResourcesRequired
        4.5.28 Interface SVGFitToViewBox
        4.5.29 Interface SVGZoomAndPan
        4.5.30 Interface SVGViewSpec
        4.5.31 Interface SVGURIReference
        4.5.32 Interface SVGCSSRule
        4.5.33 Interface SVGRenderingIntent




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