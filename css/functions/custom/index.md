{{Page_Title|custom()}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections
|Content=Incomplete
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|With CSS custom filters you can create your own sophisticated effects on DOM elements. They work with CSS animations and transitions to create complex animated visual effects.}}
{{CSS_Function}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=Using shaders created by Adobe, the following example shows how to create a folded map effect with custom CSS filters.
|Code=<!DOCTYPE html>
<html>
<head>
  <style>
    #map {
      width: 400px;
      height: 400px;
      -webkit-transform: translate3d(0px, 0px, 0px);
      -webkit-filter: custom(
        url(http://html.adobe.com/webstandards/csscustomfilters/cssfilterlab/shaders/vertex/fold.vs) mix(url(http://html.adobe.com/webstandards/csscustomfilters/cssfilterlab/shaders/fragment/fold.fs) multiply source-atop), 
        8 50, 
        transform perspective(1000) scale(1) rotateX(0deg) rotateY(0deg) rotateZ(0deg), 
        t 0.5, 
        spins 1.5, 
        phase -0.7, 
        shadow 1.5, 
        mapDepth 40, 
        mapCurve -0.3, 
        minSpacing 0.3, 
        useColoredBack 1, 
        backColor 0.5 0.5 0.5 1
      );  
    }
  </style>
</head>
<body>
  <img src="http://maps.googleapis.com/maps/api/staticmap?center=51.58803,4.774246&zoom=15&size=400x400&sensor=false" id="map" />
</body>
</html>
|LiveURL=http://codepen.io/pverbeek/pen/piKgC
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=No
|Chrome_version=
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
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
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=No
|Safari_prefixed_version=
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
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Google Chrome Canary
|Note=Currently only available in Google Chrome Canary. In Canary, enter “about:flags” in the address bar, find “Enable CSS Shaders”, click “Enable”, and relaunch Canary
}}
}}
{{See_Also_Section
|Topic_clusters=Filters
|External_links=* [http://www.khronos.org/files/opengles_shading_language.pdf OpenGL ES Shading Language (PDF)]
* [http://html.adobe.com/webstandards/csscustomfilters/cssfilterlab/ Adobe CSS FilterLab]
* [http://www.adobe.com/devnet/html5/articles/css-shaders.html Introducing CSS shaders]
}}
{{Topics|CSS, Graphics, SVG}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}