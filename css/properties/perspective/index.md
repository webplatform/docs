{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Perspective defines how an object is viewed. In graphic arts, perspective is the representation on a flat surface of what the viewer's eye would see in a 3D space. If there were a window between the viewer and the object, you could project points on the window surface that correspond to the points that exist beyond the glass. (See [http://en.wikipedia.org/wiki/Perspective_(graphical) Wikipedia] for more information about graphical perspective and for related illustrations.)

The illusion of perspective on a flat surface, such as a computer screen, is created by projecting points on the flat surface as they would appear if the flat surface were a window through which the viewer was looking at the object. In discussion of virtual environments, this flat surface is called a projection plan.

The perspective property defines how far an element is placed from the view on the z-axis, from the screen to the viewer.
}}
{{CSS Property
|Initial value=none
|Applies to=transformable elements
|Inherited=No
|Media=visual
|Computed value=Absolute length or "none"
|Animatable=No
|Values={{CSS Property Value
|Data Type=none
|Description=Default.
}}{{CSS Property Value
|Data Type=[[css/data_types/length|<length>]]
|Description=The distance the element is places on the z-axis. Lengths must be positive
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example shows the difference with transforms, where one has a perspective set to it.
|Code=&lt;!DOCTYPE html&gt;
&lt;html&gt;
  &lt;head&gt;
    &lt;title&gt;Perspective example&lt;/title&gt;
    &lt;style&gt;
      .foo {
        margin: 0 100px;
        float: left;
      }

      .bar {
        -webkit-perspective: 800px;
        -moz-perspective: 800px;
        perspective: 800px;
      }

      .foo img {
        -webkit-transform: rotateX(-60deg);
        -moz-transform: rotateX(-60deg);
        transform: rotateX(-60deg);
      }
    &lt;/style&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;div class=&quot;foo bar&quot;&gt;
      &lt;img src=&quot;http://www.webplatform.org/logo/wplogo_transparent_xlg.png&quot; /&gt;
    &lt;/div&gt;

    &lt;div class=&quot;foo baz&quot;&gt;
      &lt;img src=&quot;http://www.webplatform.org/logo/wplogo_transparent_xlg.png&quot; /&gt;
    &lt;/div&gt;
  &lt;/body&gt;
&lt;/html&gt;
|LiveURL=http://codepen.io/pverbeek/pen/rgnla
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Transforms
|URL=http://www.w3.org/TR/css3-transforms/#perspective-property
|Status=Working Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=No
|Chrome_version=
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=12
|Firefox_supported=Yes
|Firefox_version=16.0
|Firefox_prefixed_supported=Yes
|Firefox_prefixed_version=10.0
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=Yes
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=No
|Android_version=
|Android_prefixed_supported=Yes
|Android_prefixed_version=3.0
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=16.0
|Firefox_mobile_prefixed_supported=Yes
|Firefox_mobile_prefixed_version=10.0
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
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
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Transforms
|Manual_links=* [[tutorials/css_transforms#You_need_some_perspective|Manipulating content with CSS3 transforms, You need some perspective]] by [[User:Sierra|Mike Sierra]]
|External_links=* [http://sandbox.webpro.nl/css3/3d-transforms-interactive-demo.html CSS 3D Transforms: Interactive Demo] by [https://twitter.com/webprolific Lars Kappert]
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}