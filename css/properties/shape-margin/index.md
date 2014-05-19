{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Adds a margin to a [[css/properties/shape-outside|shape-outside]]. In effect, defines a new shape that is the smallest contour around all the points that are the ''shape-margin'' distance outward perpendicular to each point on the underlying shape. For points where a perpendicular direction is not defined (e.g., a triangle corner), takes all points on a circle centered at the point and with a radius of the ''shape-margin'' distance. This property accepts only non-negative values.}}
{{CSS Property
|Initial value=0
|Applies to=Floats
|Inherited=No
|Media=visual
|Computed value=as specified, but with lengths made absolute
|Animatable=No
|Values={{CSS Property Value
|Data Type=<length>
|Description=Sets the margin of the shape to the <length>.
}}{{CSS Property Value
|Data Type=<percentage>
|Description=Sets the margin of the shape to a percentage of the width of the element’s containing block.
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
|LiveURL=http://code.webplatform.org/gist/8080942aab7bad2d1c2f
}}{{Single Example
|Language=CSS
|Description=In the CSS class, we float the image left, set its shape to be the same image, and then we set a margin of 30px.
|Code=.shape {    
	float  : left;    
	shape-outside : url("http://openclipart.org/image/800px/svg_to_png/10312/Odysseus_Blue_flower.png");    
	shape-margin : 30px;    
}
|LiveURL=http://code.webplatform.org/gist/6500717
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Shapes Module Level 1
|URL=http://www.w3.org/TR/css-shapes/
|Status=W3C Candidate Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables={{Imported Compatibility Table}}
|Desktop_rows=
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Safari
|Version=538+
|Note=Using vendor prefix -webkit-
}}
}}
{{See_Also_Section
|Manual_links=[[css/properties/shape-outside|shape-outside]]
[[css/properties/shape-image-threshold|shape-image-threshold]]
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}