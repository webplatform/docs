{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Perspective-origin changes the appearance of an object, as if a viewer were looking at it from a different origin. An object appears differently if a viewer is looking directly at it versus looking down at it, looking up at it, or from the side.

When used with the [[css/properties/perspective|perspective]] property, the default value of perspective-origin is 50% 50%. This displays an object as if the viewer's eye were positioned directly at the center of the screen, both top-to-bottom and left-to-right. A value of 0% 0% changes the object as if it were being viewed from the top left angle. A value of 100% 100% changes the appearance as if viewed from the bottom right angle.
}}
{{CSS Property
|Initial value=50% 50%
|Applies to=transformable elements
|Inherited=No
|Media=visual
|Computed value=length: the absolute value; otherwise, a percentage
|Animatable=No
|CSS object model property=perspectiveOrigin
|CSS percentages=The size of the bounding box
|Values={{CSS Property Value
|Data Type=<length>
|Description=A floating-point number, followed by either an absolute units designator
(cm, mm, in, pt, or pc) or a relative units designator
(em, ex, or px), that indicates the origin of transformation.
}}{{CSS Property Value
|Data Type=<percentage>
|Description=An integer, followed by a %. The value is a percentage of the total box length (for the first value) or the total box height (for the second value, if specified). The default is 50% 50%, as if the viewer was positioned directly in front of the object.
}}{{CSS Property Value
|Data Type=left
|Description=First value only. Equal to 0% or a zero length. Displays the object as if the viewer were looking from the left.
}}{{CSS Property Value
|Data Type=right
|Description=First value only. Equal to 100% or the full box length. Displays the object as if the viewer were looking from the right.
}}{{CSS Property Value
|Data Type=top
|Description=Second value only. Equal to 0% or a zero height. Displays the object as if the viewer were looking from the top.
}}{{CSS Property Value
|Data Type=bottom
|Description=Second value only. Equal to 100% or the full box height. Displays the object as if the viewer were looking from the bottom.
}}{{CSS Property Value
|Data Type=center
|Description=Equal to 50% or half the length of the box. When given as the first value, displays the object as if the viewer was positioned on par with the object, from left-to-right.
}}{{CSS Property Value
|Data Type=center
|Description=Equal to 50% or half the height of the box. When given as the second value, displays the object as if the viewer was positioned on par with the object, from top-to-bottom.
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=This property requires the [[css/properties/perspective|'''perspective''']] property. perspective-origin has no effect on the child elements if the [[css/properties/perspective|'''perspective''']] property is not set for the object.

If only one value is specified, the second value is assumed to be center. If at least one of the two values is not a keyword, then the first value represents the horizontal position (or offset) and the second represents the vertical position (or offset).
|Notes=Perspective defines how an object is viewed. In graphic arts, perspective is the representation on a flat surface of what the viewer's eye would see in a 3D space. If there were a window between the viewer and the object, you could project points on the window surface that correspond to the points that exist beyond the glass. (See [http://en.wikipedia.org/wiki/Perspective_(graphical) Wikipedia] for more information about graphical perspective and for related illustrations.)

The illusion of perspective on a flat surface, such as a computer screen, is created by projecting points on the flat surface as they would appear if the flat surface were a window through which the viewer was looking at the object. In discussion of virtual environments, this flat surface is called a projection plane. 

The perspective-origin sets the virtual position of the viewer. As perspective-origin-x changes, the virtual eye moves along the x axis (left or right of the center of the screen). As perspective-origin-y changes, the eye moves along the y axis (closer to the top or bottom of the screen).
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS3 Transforms, The ‘perspective-origin’ Property
|URL=http://dev.w3.org/csswg/css-transforms/#perspective-origin-property
|Status=W3C Editor's Draft
|Relevant_changes=Order of values
}}{{Related Specification
|Name=CSS3 Transforms, The ‘perspective-origin’ Property
|URL=http://www.w3.org/TR/css3-transforms/#perspective-origin-property
|Status=W3C Working Draft
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
|Topic_clusters=Transforms
|Manual_links=* [[tutorials/css_transforms#You_need_some_perspective|Manipulating content with CSS3 transforms, You need some perspective]] by [[User:Sierra|Mike Sierra]]
|External_links=* [http://sandbox.webpro.nl/css3/3d-transforms-interactive-demo.html CSS 3D Transforms: Interactive Demo] by [https://twitter.com/webprolific Lars Kappert]
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}