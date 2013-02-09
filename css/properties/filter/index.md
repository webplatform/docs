{{Page_Title|filter}}
{{Flags}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Applies various image processing effects.}}
{{CSS Property
|Initial value=none
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Computed value=as specified
|Animatable=Yes
|CSS object model property=filter
|Values={{CSS Property Value
|Data Type=<functions>
|Description=Any combination of built-in filter functions, executed in sequence: [[css/functions/blur|'''blur()''']], [[css/functions/brightness|'''brightness()''']], [[css/functions/contrast|'''contrast()''']], [[css/functions/drop-shadow|'''drop-shadow()''']], [[css/functions/grayscale|'''grayscale()''']], [[css/functions/hue-rotate|'''hue-rotate()''']], [[css/functions/invert|'''invert()''']], [[css/functions/opacity|'''opacity()''']], [[css/functions/saturate|'''saturate()''']], and [[css/functions/sepia|'''sepia()''']]
}}
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Usage=Filters apply any combination of image processing functions to
visual elements.  This example shows how a combination of more than
one filter function may affect an image:

 filter: grayscale(100%) sepia(100%);

[[Image:f01-pencil.jpg|300px]]&nbsp;[[Image:f04-graysepia.jpg|300px]]

Filters are applied to the image data in sequence, so the order in
which functions are declared makes a difference. If the
[[css/functions/sepia|'''sepia()''']] function were applied before the
[[css/functions/grayscale|'''grayscale()''']] in the example above,
the image would appear completely gray rather than slightly yellowed.

Filters apply to any graphic effect the element renders, such as
borders, background images, scrollbars, letterforms, text selections,
even videos.  Each filter also applies to the cumulative effect of
previously declared filters. (The same function may be applied
repeatedly.) Both the [[css/functions/blur|'''blur()''']] and
[[css/functions/drop-shadow|'''drop-shadow()''']]
filters may render pixels outside the original content box,
and when paired with other CSS properties such as 
[[css/properties/opacity|'''opacity''']], these pixels may
become clipped.

Filter effects may be specified as part of dynamic
[[tutorials/css_transitions#advanced|transitions]] and
[[tutorials/css_animations|keyframe animations]]. However, the number
of functions in each set of style sheets must match, with no
transitions allowed from implied default values. In addition, each
style sheet must declare the exact same sequence of functions.

==Built-in filter functions==

The following examples show the effect of each filter function applied
in isolation. See each function for details on accepted parameters.

[[css/functions/brightness|'''brightness(1.4)''']]

[[Image:f17-boatonlake2.jpg|300px]]&nbsp;[[Image:f18-boatonlake2bright.jpg|300px]]

[[css/functions/contrast|'''contrast(2)''']]

[[Image:f19-jellybeans.jpg|300px]]&nbsp;[[Image:f20-jellybeancontrast.jpg|300px]]

[[css/functions/grayscale|'''grayscale(1)''']]

[[Image:f05-boatonlake.jpg|300px]]&nbsp;[[Image:f06-boatonlakegray.jpg|300px]]

[[css/functions/sepia|'''sepia(1)''']]

[[Image:f07-lenna.jpg|300px]]&nbsp;[[Image:f08-lennasepia.jpg|300px]]

[[css/functions/invert|'''invert(1)''']]

[[Image:f13-peppers.jpg|300px]]&nbsp;[[Image:f14-peppersinvert.jpg|300px]]

[[css/functions/hue-rotate|'''hue-rotate(90deg)''']]

[[Image:f11-mandrill.jpg|300px]]&nbsp;[[Image:f12-mandrillhuerotate.jpg|300px]]

[[css/functions/saturate|'''saturate(10)''']]

[[Image:f09-tiffany.jpg|300px]]&nbsp;[[Image:f10-tiffanysaturate.jpg|300px]]

[[css/functions/opacity|'''opacity(0.5)''']]

[[Image:f15-splash.jpg|300px]]&nbsp;[[Image:f16-splashopacity50.jpg|300px]]

[[css/functions/blur|'''blur(10px)''']]

[[Image:f21-peppers2.jpg|300px]]&nbsp;[[Image:f22-peppers2blur.jpg|300px]]

[[css/functions/drop-shadow|'''drop-shadow(16px 16px 20px black)''']]

[[Image:f11-mandrill.jpg|300px]]&nbsp;[[Image:f23-mandrilldrop1.jpg|300px]]
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Filter Effects 1.0
|URL=https://dvcs.w3.org/hg/FXTF/raw-file/tip/filters/index.html#
|Status=Editor's Draft
}}{{Related Specification
|Name=Filter Effects 1.0
|URL=http://www.w3.org/TR/filter-effects/
|Status=Working Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=21.0
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=No
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Yes
|Safari_prefixed_version=6.0
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=No
|Android_version=
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=No
|Blackberry_version=
|Blackberry_prefixed_supported=No
|Blackberry_prefixed_version=
|Chrome_mobile_supported=No
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=No
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=No
|IE_mobile_version=
|IE_mobile_prefixed_supported=No
|IE_mobile_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Yes
|Safari_mobile_prefixed_version=6.0
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Filters
|External_links=* W3C editor's draft: [https://dvcs.w3.org/hg/FXTF/raw-file/tip/filters/index.html# Filter Effects 1.0]
* [http://html5-demos.appspot.com/static/css/filters/index.html Interactive demonstration]
}}
{{Topics|CSS, Graphics, SVG}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=HTML5Rocks
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=http://www.html5rocks.com/en/tutorials/filters/understanding-css/
}}