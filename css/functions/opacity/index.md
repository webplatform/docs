{{Page_Title|opacity()}}
{{Flags}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Applies a transparency effect to an element's
colors, for use by the [[css/properties/filter|'''filter''']]
property. A decimal value between 0 and 1 or percentage up to 100%
controls the overall opacity, with 0 rendering the element invisible
and background elements showing through.
}}
{{CSS_Function
|Content=This CSS property value is reflected in the following image:

 filter: opacity(50%);
 filter: opacity(0.5);

[[Image:f15-splash.jpg|300px]]&nbsp;[[Image:f16-splashopacity50.jpg|300px]]

When used in isolation, the '''opacity()''' filter has the same effect
as the [[css/properties/opacity|'''opacity''']] CSS property, but it
produces different effects when used in conjunction with other
filters.  The second example below produces a shadow that shows
through the image, and the third doesn't when functions execute in
reverse order:

 filter: none;
 filter: opacity(0.5) drop-shadow(10px 10px 0px black);
 filter: drop-shadow(10px 10px 0px black) opacity(0.5);

[[Image:opacitySequence.png]]

'''Note:''' As is true for the related
[[css/properties/opacity|'''opacity''']] CSS property, transparent
elements still receive mouse and touch events, but the
[[css/properties/pointer-events|'''pointer-events''']] property offers
a way to override this behavior.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following example shows the difference between two images, where one has an opacity of 50%:

[[Image:filter_opacity1.png|400px]]
|Code=&lt;!DOCTYPE html&gt;
&lt;html&gt;
  &lt;head&gt;
    &lt;title&gt;Filter example&lt;/title&gt;
    &lt;style&gt;
      .foo {
        float: left;
      }

      .bar { 
        -webkit-filter: opacity(50%);
      }
    &lt;/style&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;img src=&quot;http://www.webplatform.org/logo/wplogo_transparent_xlg.png&quot; class=&quot;foo&quot; /&gt;
    &lt;img src=&quot;http://www.webplatform.org/logo/wplogo_transparent_xlg.png&quot; class=&quot;foo bar&quot; /&gt;
  &lt;/body&gt;
&lt;/html&gt;
|LiveURL=http://codepen.io/pverbeek/pen/qhfaD
}}{{Single Example
|Language=HTML
|Description=This example shows the importance of the order in which filters are applied. 
In the first image, the opacity is only applied to the image.
In the second, the drop-shadow is applied first, so the opacity also applies to it.

[[Image:filter_opacity2.png|400px]]
|Code=&lt;!DOCTYPE html&gt;
&lt;html&gt;
  &lt;head&gt;
    &lt;title&gt;Filter example&lt;/title&gt;
    &lt;style&gt;
      .foo {
        float: left;
      }

      .bar { 
        -webkit-filter: opacity(.5) drop-shadow(1px 1px 20px black);
      }

      .baz { 
        -webkit-filter: drop-shadow(1px 1px 20px black) opacity(.5);
      }
    &lt;/style&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;img src=&quot;http://www.webplatform.org/logo/wplogo_transparent_xlg.png&quot; class=&quot;foo bar&quot; /&gt;
    &lt;img src=&quot;http://www.webplatform.org/logo/wplogo_transparent_xlg.png&quot; class=&quot;foo baz&quot; /&gt;
  &lt;/body&gt;
&lt;/html&gt;
|LiveURL=http://codepen.io/pverbeek/pen/KzEHw
}}
}}
{{Notes_Section}}
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
|External_links=* [http://html.adobe.com/webstandards/csscustomfilters/cssfilterlab/ Adobe CSS FilterLab]
* [http://html5-demos.appspot.com/static/css/filters/index.html Interactive demonstration]
}}
{{Topics|CSS, Graphics, SVG}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}