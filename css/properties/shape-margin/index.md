{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Adds a margin to a [[css/properties/shape-outside|shape-outside]]. In effect, defines a new shape that is the smallest contour around all the points that are the ''shape-margin'' distance outward perpendicular to each point on the underlying shape. For points where a perpendicular direction is not defined (e.g., a triangle's corner), takes all points on a circle centered at the point and with a radius of the ''shape-margin'' distance. This property accepts only non-negative values.}}
{{CSS Property
|Initial value=0
|Applies to=Floats
|Inherited=No
|Media=visual
|Computed value=The absolute length
|Animatable=No
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=<length>
|Description=The distance, in pixels, that is used to calculate the "outer margin" shape's offset from the original shape.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=In the following example, we have an image with a CSS class and a paragraph wrapped in a P tag.
|Code=&lt;p&gt;
  &lt;img class=&quot;logo&quot; src=&quot;http://docs.webplatform.org/w/skins/webplatform/images/logo.png&quot;/&gt;

  We are an open community of developers building resources for a better web, regardless of brand, browser or platform. Anyone can contribute and each person who does makes us stronger. Together we can continue to drive innovation on the Web to serve the greater good. It starts here, with you.
&lt;/p&gt;
|LiveURL=http://code.webplatform.org/gist/6500717
}}{{Single Example
|Language=CSS
|Description=In the CSS class, we float the image left, set its shape to be the same image, and then we set a margin of 16px.
|Code=.logo {
    float  : left;
    shape-outside : url("http://docs.webplatform.org/w/skins/webplatform/images/logo.png");
    shape-margin : 16px;
}
|LiveURL=http://code.webplatform.org/gist/6500717
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Shapes Module Level 1
|URL=* http://www.w3.org/TR/css-shapes/
|Status=W3C Editor's Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables={{Imported Compatibility Table}}
|Desktop_rows=
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=10
|Note=Uses a vendor prefixed version of an old name of this property - wrap-margin.
}}{{Compatibility Notes Row
|Browser=Chrome
|Version=25.0.1364.160
|Note=Using vendor prefix -webkit-
}}{{Compatibility Notes Row
|Browser=Opera
|Version=12.14
|Note=Using vendor prefix -o-
}}{{Compatibility Notes Row
|Browser=FireFox
|Version=19
|Note=Using vendor prefix -moz-
}}{{Compatibility Notes Row
|Browser=Safari
|Version=534.57.2
|Note=Using vendor prefix -webkit-
}}
}}
{{See_Also_Section
|Manual_links=[[css/properties/wrap-flow|wrap-flow]]
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/windows/apps/hh466103.aspx
|HTML5Rocks_link=
}}