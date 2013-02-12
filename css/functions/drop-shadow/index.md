{{Page_Title|drop-shadow()}}
{{Flags}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Applies a shadow to an element's pixels, for use by
the [[css/properties/filter|'''filter''']] property.  Accepts up to 3
distance measurements, representing ''x''/''y'' offset and blur
radius, along with a color value.
}}
{{CSS_Function
|Content=This CSS property value is reflected in the following images:

 filter: drop-shadow(16px 16px 20px black);   /* left */
 filter: drop-shadow(10px -16px 30px purple); /* right */

[[Image:f23-mandrilldrop1.jpg|300px]]&nbsp;[[Image:f24-mandrillshadow2.jpg|300px]]

Setting offsets to 0 with a positive blur value produces a
backlit halo effect.  Setting blur to 0 and positive offset values
produces a raised effect as if sunlight is falling on the element.
The '''drop-shadow()''' function uses the same syntax as the
[[css/properties/text-shadow|'''text-shadow''']] CSS property, and
likewise allows for more than one set of shadow values, separated with
commas. This example renders both of the shadows shown above:

 filter: drop-shadow(16px 16px 20px black, 10px -16px 30px purple);

The filter affects the contours of image transparencies, which
allows for more vivid shadow effects:

[[Image:giraffe_dropshadow.png]]
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The below example shows the difference between the CSS box-shadow property and the drop-shadow filter function. Where the box-shadow property outlines the html box and the drop-shadow outlines the element parts.
|Code=&lt;!DOCTYPE html&gt;
&lt;html&gt;
  &lt;head&gt;
    &lt;title&gt;Filter example&lt;/title&gt;
    &lt;style&gt;
      .foo {
        width: 100px;
        padding: 50px 0;
        margin: 100px;
        text-align: center;
        border: dashed 10px red;
        float: left;
      }

      .bar {
        box-shadow: 5px 5px 10px black;
      }

      .baz {
        -webkit-filter: drop-shadow(5px 5px 10px black);
      }
    &lt;/style&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;div class=&quot;foo bar&quot;&gt;&lt;/div&gt;
    &lt;div class=&quot;foo baz&quot;&gt;&lt;/div&gt;
  &lt;/body&gt;
&lt;/html&gt;
|LiveURL=http://codepen.io/pverbeek/pen/etIyE
}}{{Single Example
|Description=This example shows the difference when using png images with transparency.
|Code=&lt;!DOCTYPE html&gt;
&lt;html&gt;
  &lt;head&gt;
    &lt;title&gt;Filter example&lt;/title&gt;
    &lt;style&gt;
      .foo {
        float: left;
      }

      .bar {
        box-shadow: 5px 5px 10px black;
      }

      .baz {
        -webkit-filter: drop-shadow(5px 5px 10px black);
      }
    &lt;/style&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;img src=&quot;http://www.webplatform.org/logo/wplogo_transparent_xlg.png&quot; class=&quot;foo&quot; /&gt;
    &lt;img src=&quot;http://www.webplatform.org/logo/wplogo_transparent_xlg.png&quot; class=&quot;foo bar&quot; /&gt;
  &lt;/body&gt;
  &lt;/body&gt;
&lt;/html&gt;
|LiveURL=http://codepen.io/pverbeek/pen/BlFef
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
|External_links=* W3C editor's draft: [https://dvcs.w3.org/hg/FXTF/raw-file/tip/filters/index.html# Filter Effects 1.0]
* [http://html5-demos.appspot.com/static/css/filters/index.html Interactive demonstration]
}}
{{Topics|CSS, Graphics, SVG}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}