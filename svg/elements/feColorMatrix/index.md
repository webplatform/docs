{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic
|Content=Incomplete, Cleanup, Compatibility Incomplete, Examples Needed, Examples Best Practices
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|feColorMatrix is an SVG filter primitive that allows the manipulation of color values across color channels. It provides more powerful color manipulation flexibility than CSS shorthand filters. It is always a child element of an SVG filter element. Using feColorMatrix, you can change color saturation, perform hue rotations, selectively adjust alpha values of particular channels, adjust contrast, brightness and more. feColorMatrix does not allow the manipulation of relative color values *within* color channels which is provided by the feComponentTransfer primitive.}}
{{Markup_Element
|DOM_interface=svg/objects/SVGFEColorMatrixElement
|Content=feColorMatrix is a filter primitive that allows the manipulation of color values across color channels. It is always a child element of a [[http://docs.webplatform.org/wiki/svg/elements/filter |filter element]]. Using feColorMatrix, you can change color saturation, perform hue rotations, selectively adjust alpha values of particular channels, adjust contrast, brightness and more. feColorMatrix does not allow the manipulation of relative color values *within* color channels which is provided by the feComponentTransfer primitive. 

Attributes:

* in (optional): specifies the input graphic. If "in" is ommitted; and feColorMatrix is the first primitive in a filter, the default value is SourceGraphic. Otherwise, the immediately preceding primitive's result is used as input. Permitted values for "in" are described below.
* result (optional): creates a reference for the primitive's result that other primitives can use as the value of their "in" or "in2" attributes.
* color-interpolation-filters (optional): permitted values are "linearRGB" (default) and "sRGB".
* x, y, width, height (optional): default to the size of the parent filter region.

Other standard SVG element attributes (style, id, class etc.) may also be added to the element.  Like all filter primitives that accept an input, feColorMatrix can accept the following values as input via the "in" attribute.

* SourceGraphic: the target element(image, shape, group etc.) that references the filter
* SourceAlpha: a graphic containing just the alpha channel of the target element.
* BackgroundImage: the canvas beneath the SourceGraphic (requires a correctly specified "enable-background" attribute. (limited browser support as of Dec '12)
* BackgroundAlpha: the alpha channel of the canvas beneath the SourceGraphic (requires a correctly specified "enable-background" attribute. Limited browser support as of Dec '12)
* FillPaint: a pseudo-graphic equal to the size of the filter region filled with the fill property of the target element (limited browser support as of Dec '12)
* StrokePaint: a pseudo-graphic equal to the size of the filter region filled with the stroke property of the target element (limited browser support as of Dec '12)
* Primitive reference: the "result" of another primitive.

feColorMatrix offers four types of color manipulation: 3 shorthands and a matrix manipulation:

* saturate: adjusts the saturation of all RGB color channels (the alpha channel is not affected). The permitted value according to the specification is 0-1, but many browsers accept higher values >1 to allow over-saturation.
* hueRotate: adjusts the hue of all RGB color channels (the alpha channel is not affected)
* luminanceToAlpha: discards the alpha channel and replaces it with values equal to the input's luminance. The RGB channels are set to black (0,0,0).
* matrix: a superset of the shorthands. Allows the value of each channel in the output to be specified from a combination of its existing color and alpha channels.

(It's important to note that manipulations are applied to *non-pre-multiplied" values*.  This means that alpha adjustments (aka. opacity) are unapplied before calculations are performed. This means, for example, that colors that appear similar same visually on a white background (eg. rgba(255,0,0,.5) and rgba(128,0,0,1) can look very different after a feColorMatrix operation. For example, a "saturate=2" will have no effect on the first color, but dramatically redden the second color.)

By default, color-manipulation operations using feColorMatrix take place in linearRGB color space. This may produce unwanted results. For example a color inversion may result in a pronounced shift toward lighter tones. If this is not desired, you may explicitly specify a value of "sRGB" for the optional attribute "color-interpolation-filters".
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=Other
|Description=Example of a feColorMatrix with type="saturate"
|Code=<syntaxhighlight lang="xml">
<svg width="640" height="550" viewBox="0 0 640 550">
<defs>
    <filter id="saturate">
      <feColorMatrix in="SourceGraphic" type="saturate" values=".5" result="A"/>
   </filter>
  </defs>
  <image x="10" y="10" width="280" height="350" preserveAspectRatio="true" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>
  <image x="310" y="10" width="280" height="350" preserveAspectRatio="true" filter="url(#saturate)" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>
</svg>​
</syntaxhighlight>
|LiveURL=http://code.webplatform.org/gist/5303882
}}{{Single Example
|Language=Other
|Description=Example of a feColorMatrix with type="hueRotate"
|Code=<svg width="640" height="550" viewBox="0 0 640 550">
<defs>
    <filter id="hueRotate">
      <feColorMatrix in="SourceGraphic" type="hueRotate" values="45" result="A"/>
   </filter>
  </defs>
  <image x="10" y="10" width="280" height="350" preserveAspectRatio="true" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>
  <image x="310" y="10" width="280" height="350" preserveAspectRatio="true" filter="url(#hueRotate)" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>
</svg>​
|LiveURL=http://code.webplatform.org/gist/5303933
}}{{Single Example
|Language=Other
|Description=Example of a feColorMatrix with type="luminanceToAlpha"
|Code=<svg width="640" height="550" viewBox="0 0 640 550">
<defs>
    <filter id="L2A">
      <feColorMatrix in="SourceGraphic" type="luminanceToAlpha" result="A"/>
   </filter>
  </defs>
  <image x="10" y="10" width="280" height="350" preserveAspectRatio="true" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>
  <image x="310" y="10" width="280" height="350" preserveAspectRatio="true" filter="url(#L2A)" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>
</svg>​
|LiveURL=http://code.webplatform.org/gist/5303960
}}{{Single Example
|Language=Other
|Description=Example of a feColorMatrix with type="matrix" showing a contrast adjustment
|Code=<svg width="640" height="550" viewBox="0 0 640 550">
<defs>
    <filter id="matrix-contrast">
      <feColorMatrix in="SourceGraphic" type="matrix" values="1.2 0 0 0 -0.2 
                                                              0 1.2 0 0 -0.2 
                                                              0 0 1.2 0 -0.2
                                                              0 0 0 1 0"/>
   </filter>
  </defs>
  <image x="10" y="10" width="280" height="350" preserveAspectRatio="true" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>
  <image x="310" y="10" width="280" height="350" preserveAspectRatio="true" filter="url(#matrix-contrast)" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>
</svg>​
|LiveURL=http://code.webplatform.org/gist/5304023
}}{{Single Example
|Language=Other
|Description=Example of a feColorMatrix with type="matrix" showing a sepia adjustment
|Code=<svg width="640" height="550" viewBox="0 0 640 550">
<defs>
    <filter id="matrix-sepia">
      <feColorMatrix in="SourceGraphic" type="matrix" values=".35 .35 .35 0 0 
                                                              .25 .25 .25 0 0 
                                                              .15 .15 .15 0 0
                                                              0 0 0 1 0"/>
   </filter>
  </defs>
  <image x="10" y="10" width="280" height="350" preserveAspectRatio="true" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>
  <image x="310" y="10" width="280" height="350" preserveAspectRatio="true" filter="url(#matrix-sepia)" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>
</svg>​
|LiveURL=http://code.webplatform.org/gist/5304047
}}{{Single Example
|Language=Other
|Description=Example of a feColorMatrix with type="matrix" showing a standard greyscale adjustment
|Code=<svg width="640" height="550" viewBox="0 0 640 550">
<defs>
    <filter id="matrix-greyscale">
      <feColorMatrix in="SourceGraphic" type="matrix" values=".33 .33 .33 0 0 
                                                              .33 .33 .33 0 0 
                                                              .33 .33 .33 0 0
                                                              0 0 0 1 0"/>
   </filter>
  </defs>
  <image x="10" y="10" width="280" height="350" preserveAspectRatio="true" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>
  <image x="310" y="10" width="280" height="350" preserveAspectRatio="true" filter="url(#matrix-greyscale)" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>
</svg>​
|LiveURL=http://code.webplatform.org/gist/5304064
}}{{Single Example
|Language=Other
|Description=Example of a feColorMatrix with type="matrix" showing a greyscale with green channel weighting
|Code=<svg width="640" height="550" viewBox="0 0 640 550">
<defs>
    <filter id="matrix-greyscale-greenboost">
      <feColorMatrix in="SourceGraphic" type="matrix" values=".25 .5 .25 0 0 
                                                              .25 .5 .25 0 0 
                                                              .25 .5 .25 0 0
                                                              0 0 0 1 0"/>
   </filter>
  </defs>
  <image x="10" y="10" width="280" height="350" preserveAspectRatio="true" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>
  <image x="310" y="10" width="280" height="350" preserveAspectRatio="true" filter="url(#matrix-greyscale-greenboost)" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>
</svg>​
|LiveURL=http://code.webplatform.org/gist/5304095
}}{{Single Example
|Language=Other
|Description=Example of a feColorMatrix with type="matrix" showing a a solarization effect. Each color channel is zero'd and replaced with the average of the others.
|Code=<svg width="640" height="550" viewBox="0 0 640 550">
<defs>
    <filter id="matrix-solarize">
      <feColorMatrix in="SourceGraphic" type="matrix" values="-1 .5 .5 0 0 
                                                              .5 -1 .5 0 0 
                                                              .5 .5 -1 0 0
                                                              0 0 0 1 0"/>
   </filter>
  </defs>
  <image x="10" y="10" width="280" height="350" preserveAspectRatio="true" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>
  <image x="310" y="10" width="280" height="350" preserveAspectRatio="true" filter="url(#matrix-solarize)" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>
</svg>​
|LiveURL=http://code.webplatform.org/gist/5304157
}}{{Single Example
|Language=Other
|Description=Example of a feColorMatrix with type="matrix" showing an inversion
|Code=<svg width="640" height="550" viewBox="0 0 640 550">
<defs>
    <filter id="matrix-invert">
      <feColorMatrix in="SourceGraphic" type="matrix" values="-1 0 0 0 1 
                                                              0 -1 0 0 1 
                                                              0 0 -1 0 1
                                                              0 0 0 1 0"/>
   </filter>
  </defs>
  <image x="10" y="10" width="280" height="350" preserveAspectRatio="true" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>
  <image x="310" y="10" width="280" height="350" preserveAspectRatio="true" filter="url(#matrix-invert)" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>
</svg>​
|LiveURL=http://code.webplatform.org/gist/5304176
}}
}}
{{Notes_Section
|Notes====Remarks===

This filter applies the following matrix transformation:

 {{!}} R' {{!}}     {{!}} a00 a01 a02 a03 a04 {{!}}   {{!}} R {{!}}
 {{!}} G' {{!}}     {{!}} a10 a11 a12 a13 a14 {{!}}   {{!}} G {{!}}
 {{!}} B' {{!}}  =  {{!}} a20 a21 a22 a23 a24 {{!}} * {{!}} B {{!}}
 {{!}} A' {{!}}     {{!}} a30 a31 a32 a33 a34 {{!}}   {{!}} A {{!}}
 {{!}} 1  {{!}}     {{!}}  0   0   0   0   1  {{!}}   {{!}} 1 {{!}}

This matrix is applied on the RGBA color and alpha values of every
pixel on the input graphics to produce a result with a new set of RGBA
color and alpha values.

The calculations are performed on non-premultiplied color values. If
the input graphics consist of premultiplied color values, those values
are automatically converted into non-premultiplied color values for
this operation.
|Import_Notes====Syntax===

===Standards information===

* [http://www.w3.org/TR/SVG/filters.html#feColorMatrixElement SVG 1.1 Specification]

===Members===

The '''SVGFEColorMatrixElement''' object has these properties:

*[[svg/properties/height|'''height''']]: Gets or sets  the height of an element.
*[[svg/properties/in1|'''in1''']]: Identifies input for the given filter primitive.
*[[svg/properties/result|'''result''']]: Provides a reference for the output result of a filter.
*[[svg/properties/type (SVGFEColorMatrixElement)|'''type''']]: Indicates the type of matrix operation.
*[[svg/properties/values|'''values''']]: Numeric values for the '''feColorMatrix''' transformation matrix.
*[[svg/properties/width|'''width''']]: Defines the width of an element.
*[[svg/properties/x|'''x''']]: Gets or sets the x-coordinate value.
*[[svg/properties/y|'''y''']]: Gets or sets the y-coordinate value.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_prefixed_supported=Yes
|Safari_supported=Yes
|Safari_version=6
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=No
|Android_version=
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=Playbook OS1+, BB10
|Blackberry_prefixed_supported=No
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=No
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=iOS6
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Filters
}}
{{Topics|SVG}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}