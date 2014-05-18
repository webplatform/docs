{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The perspective property defines how far an element is placed from the view on the z-axis, from the screen to the viewer.

Perspective defines how an object is viewed. In graphic arts, perspective is the representation on a flat surface of what the viewer's eye would see in a 3D space. (See [http://en.wikipedia.org/wiki/Perspective_(graphical) Wikipedia] for more information about graphical perspective and for related illustrations.)

The illusion of perspective on a flat surface, such as a computer screen, is created by projecting points on the flat surface as they would appear if the flat surface were a window through which the viewer was looking at the object. In discussion of virtual environments, this flat surface is called a projection plane.
}}
{{CSS Property
|Initial value=none
|Applies to=Transformable elements.
|Inherited=No
|Media=visual
|Computed value=Absolute length or "none".
|Animatable=No
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=none
|Description=Default.
}}{{CSS Property Value
|Data Type=[[css/data_types/length|<length>]]
|Description=The distance the element is placed on the z-axis. Lengths must be positive.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example shows the difference with transforms, where the first image has a perspective set and the second does not.
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
        perspective: 800px;
      }

      .foo img {
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
|LiveURL=http://code.webplatform.org/gist/7086839
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
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_links=* [[tutorials/css_transforms#You_need_some_perspective|Manipulating content with CSS3 transforms - You need some perspective]] by [[User:Sierra|Mike Sierra]]
|External_links=* [http://sandbox.webpro.nl/css3/3d-transforms-interactive-demo.html CSS 3D Transforms: Interactive Demo] by [https://twitter.com/webprolific Lars Kappert]
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}