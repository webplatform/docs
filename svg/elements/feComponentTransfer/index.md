{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Data Not Semantic
|Content=Not Neutral, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|feComponentTransfer allows the independent manipulation of each color channel (including the alpha channel) in the input graphic.}}
{{Markup_Element
|DOM_interface=svg/objects/SVGComponentTransferElement
|Content=<code>feComponentTransfer</code> in combination with its child elements (feFuncR, feFuncG, feFuncB and feFuncA) allows the independent manipulation of each color channel of the input graphic. Five types of color manipulation are offered:

* identity: sets the result pixel's color channel value equal to the input value
* table: maps equal segments of a color channel to output ranges specified by a "tableValues" array 
* discrete: maps equal segments of a color channel to specific output values specified by a "tableValues" array
* linear: applies a simple linear formula (intercept + slope*input) to each input pixel's color channel value
* gamma: applies a gamma function (offset + amplitude*(input^exponent)) to each input pixel's color channel value

All color channel values are *unitized* into the range [0 -> 1] before being processed by the filter primitive regardless of what color unit system was used to specify the original color. This means, for example, that values for the gamma exponent greater than 1 will produce darker results (e.g when the exponent is equal to 2 and the input value is equal to 0.5, the output value will be a dark red ( 0.5^2 =.25).) On the contrary,values for the gamma exponent  of less than 1 will lighten the result.

By default, color-manipulation operations using feComponentTransfer take place in linearRGB color space. This may produce unwanted results. For example a color inversion may result in a pronounced shift toward lighter tones. If this is not desired, you may explicitly specify a value of "sRGB" for the optional attribute "color-interpolation-filters".

===Table and Discrete Component Transfers===
While linear and gamma transfers are readily understandable, Table and Discrete transfers can cause confusion, particularly since the SVG specification text degenerates into pure math on these subjects. However, the concepts are actually fairly straightforward. Let's take a simple example:

<syntaxhighlight lang="xml">
<feComponentTransfer>
<feFuncR type="table" tableValues="0.0 0.7 0.9 1.0"/>
</feComponentTransfer>
</syntaxhighlight>

Here, since there are 4 input values to the "tableValues" array, the primitive divides the input color channel (which remember has been unitized into values from 0 to 1) into 3 equal segments whose value ranges are:

  0.00 ... 0.33
  0.33 ... 0.66
  0.66 ... 1.00

then it maps those input ranges into the ranges specified in tableValues:

  0.00 ... 0.70
  0.70 ... 0.90  
  0.90 ... 1.00

For example, an input pixel whose red value is 0.5 - the midpoint of the second input range (0.33 to 0.66) - is mapped to the midpoint of the second output range (0.70 to 0.90), resulting in an output value of 0.80.

The following graphic illustrates how the input segments are mapped to the output segments. 

[[File:tabletransfer.png]]

Note that the start and end values for the input segments (and their number) are automatically calculated based on the number of values in "tableValues". For example, if tableValues had eleven values, then the input ranges are automatically set at (0.0 -> 0.1, 0.1 -> 0.2 all the way to 0.9 -> 1.0.) There is no capability in SVG 1.1 to customize the start and end values of input ranges.

A similar example for the discrete transfer is as follows:

<syntaxhighlight lang="xml">
<feComponentTransfer>
<feFuncR type="discrete" tableValues="0.0 0.7 0.0 1.0"/>
</feComponentTransfer>
</syntaxhighlight>

This time, since there are 4 input values to the "tableValues" array, the primitive divides the input color channel into 4 equal segments whose value ranges are:

  0.00 ... 0.25
  0.25 ... 0.50
  0.50 ... 0.75
  0.75 ... 1.00

then it maps those input ranges onto the specific values provided by the tableValues array:

  0.00
  0.70
  0.00  
  1.00

For example, an input pixel whose red value is 0.375 - the midpoint of the second input range (0.25 to 0.50) - would be mapped to the second array value of 0.70.

The following graphic illustrates how the input segments are mapped to the output segments in a discrete transfer. 

[[File:discretetransfer.png]]
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=Other
|Description=[[File:blue70sfilterexample.png]]

Example of a table component transfer. The input ranges are mapped onto continuous output ranges.
|Code=<svg width="640" height="550" viewBox="0 0 640 550">
 
<defs>
    <filter id="Blue70s" filterUnits="objectBoundingBox" 
            x="0%" y="0%" width="100%" height="100%">
      <feComponentTransfer in="SourceGraphic" result="A">
        <feFuncR type="table" tableValues="0 0.11 0.22 0.34 0.48 0.61 0.72 0.82 0.89 0.95 1"/>
        <feFuncG type="table" tableValues="0 0.08 0.16 0.26 0.38 0.5 0.62 0.73 0.82 0.87 0.9"/>
        <feFuncB type="table" tableValues="0.2 0.34 0.45 0.53 0.58 0.61 0.64 0.71 0.84 1 "/>
      </feComponentTransfer>    
</filter>

  </defs>
         
  <image x="10" y="10" width="280" height="350" preserveAspectRatio="true" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>
         
   <image x="310" y="10" width="280" height="350" preserveAspectRatio="true" filter="url(#Blue70s)" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>             
                
         
</svg>​
|LiveURL=http://jsfiddle.net/jsfmullany/rtD4A/
}}{{Single Example
|Language=Other
|Description=[[File:70sposter.png]]

Example of a discrete component transfer. The input ranges are mapped onto specific discrete output values.
|Code=<svg width="640" height="550" viewBox="0 0 640 550">
 
<defs>
    <filter id="Poster70s" filterUnits="objectBoundingBox" 
            x="0%" y="0%" width="100%" height="100%">
      <feComponentTransfer in="SourceGraphic" result="A">
        <feFuncR type="discrete" tableValues="0.0 1.0 1.0 1.0"/>
        <feFuncG type="discrete" tableValues="0.0 0.5 0.5 0.9"/>
        <feFuncB type="discrete" tableValues="0.0 0.6"/>
      </feComponentTransfer>    
</filter>

  </defs>
         
  <image x="10" y="10" width="280" height="350" preserveAspectRatio="true" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>
         
   <image x="310" y="10" width="280" height="350" preserveAspectRatio="true" filter="url(#Poster70s)" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>             
                
         
</svg>​
|LiveURL=http://jsfiddle.net/jsfmullany/LPnQ9/
}}{{Single Example
|Language=Other
|Description=[[File:70sposter.png]]

Example of a discrete component transfer. The input ranges are mapped onto specific discrete output values.
|Code=<svg width="640" height="550" viewBox="0 0 640 550">
 
<defs>
    <filter id="Poster70s" filterUnits="objectBoundingBox" 
            x="0%" y="0%" width="100%" height="100%">
      <feComponentTransfer in="SourceGraphic" result="A">
        <feFuncR type="discrete" tableValues="0.0 1.0 1.0 1.0"/>
        <feFuncG type="discrete" tableValues="0.0 0.5 0.5 0.9"/>
        <feFuncB type="discrete" tableValues="0.0 0.6"/>
      </feComponentTransfer>    
</filter>

  </defs>
         
  <image x="10" y="10" width="280" height="350" preserveAspectRatio="true" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>
         
   <image x="310" y="10" width="280" height="350" preserveAspectRatio="true" filter="url(#Poster70s)" xlink:href="http://upload.wikimedia.org/wikipedia/commons/8/82/Siberian-larch.jpg"/>             
                
         
</svg>​
}}
}}
{{Notes_Section
|Notes====Remarks===
This filter primitive performs component-wise remapping of data as follows for every pixel:
It allows operations like brightness adjustment, contrast adjustment, color balance, or thresholding.
The <code>feFuncR</code>, <code>feFuncG</code>, <code>feFuncB</code>, and<code>feFuncA</code> elements can be children of the <code>feComponentTransfer</code> element. For more information, see [[svg/elements/feFuncR|'''SVGFEFuncRElement''']].
The calculations are performed on non-premultiplied color values. If the input graphics consist of premultiplied color values, those values are automatically converted into non-premultiplied color values for this operation. (Note that the undoing and redoing of the premultiplication can be avoided if [[svg/elements/feFuncA|'''feFuncA''']] is the identity transform and all alpha values on the source graphic are set to 1.)
|Import_Notes====Syntax===



===Members===
The '''SVGFEComponentTransferElement''' object has these types of members:
*[#properties Properties]


====Properties====
The '''SVGFEComponentTransferElement''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[svg/properties/height|'''height''']]
|Gets or sets  the height of an element.
|-
|[[svg/properties/in1|'''in1''']]
|Identifies input for the given filter primitive.
|-
|[[svg/properties/result|'''result''']]
|Provides a reference for the output result of a filter.
|-
|[[svg/properties/width|'''width''']]
|Defines the width of an element.
|-
|[[svg/properties/x|'''x''']]
|Gets or sets the x-coordinate value.
|-
|[[svg/properties/y|'''y''']]
|Gets or sets the y-coordinate value.
|}
 
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=SVG 1.1
|URL=http://www.w3.org/TR/2011/REC-SVG11-20110816/
|Status=W3C Recommendation
}}
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
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=No
|Android_version=
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_prefixed_supported=No
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=IE10+
|IE_mobile_prefixed_supported=No
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=iOS6+
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Safari
|Version=All versions
|Note=Safari correctly honors <code>color-interpolation-filters="sRGB"</code> when that attribute is set on the filter primitive. (Chrome & firefox incorrectly honor this attribute when it is set on the filter element itself)
}}
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[svg/elements/feFuncR|SVGFEFuncRElement]]</code>
}}
{{Topics|Graphics, SVG}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}