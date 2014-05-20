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
|Description=In the following example, we have a div with an image with a CSS class.
|Code=&lt;div&gt;
  &lt;img class=&quot;logo&quot; src=&quot;http://openclipart.org/image/800px/svg_to_png/3201/nlyl_blue_circle.png&quot;/&gt;

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus pulvinar dolor a nulla convallis luctus. Mauris pellentesque sit amet purus non vulputate. Duis non nulla nec dui aliquet pharetra at quis turpis. Phasellus vestibulum nisl diam. Aliquam vitae dui quis nunc elementum vestibulum. Cras lobortis est id purus suscipit dictum. Suspendisse faucibus fermentum ligula, in luctus enim imperdiet ultricies. Maecenas ac eros in nisi egestas pulvinar. Cras eget luctus leo, eget euismod magna. Praesent ligula odio, pellentesque eu dapibus et, tristique id lacus. Pellentesque sit amet orci urna. Mauris tempor nulla quam, sit amet pulvinar velit malesuada eu. Aliquam erat volutpat. Sed vulputate quam id diam venenatis rutrum.

Maecenas dapibus dolor et lacus auctor, id vestibulum felis imperdiet. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Phasellus pretium condimentum cursus. Nullam porttitor nisi at orci hendrerit, vel rutrum turpis blandit. Suspendisse dictum augue risus, at accumsan justo varius sit amet. Vivamus eros urna, posuere id ornare nec, tincidunt eu nibh. Morbi molestie ipsum nec elit egestas iaculis. In viverra orci ac porta euismod. Vestibulum sed ultrices velit, quis fringilla nibh. Proin suscipit tincidunt mauris, nec venenatis dolor. Sed ultrices rhoncus velit, in molestie risus consectetur nec. In hac habitasse platea dictumst. Proin nec mattis est. Pellentesque tempor felis nec tempor convallis.

Curabitur et fermentum neque. Praesent hendrerit aliquam nunc sed aliquet. Phasellus a erat accumsan purus pretium dapibus. Duis gravida gravida dapibus. Phasellus sodales nisl sed sapien congue tempor. Vestibulum consectetur sagittis cursus. Nunc congue rhoncus tempor. Donec vestibulum nibh ut gravida placerat. Fusce sodales molestie orci non malesuada. Duis quam augue, scelerisque et justo quis, posuere rutrum nibh. Pellentesque ut sapien mattis, scelerisque neque et, ultricies leo. Suspendisse molestie est mauris, sed pharetra erat luctus vel. Vivamus faucibus placerat augue sed dictum. Nam erat ante, gravida ut purus vel, ornare pellentesque risus.
&lt;/div&gt;
|LiveURL=http://code.webplatform.org/gist/6495f066863775c4aa27
}}{{Single Example
|Language=CSS
|Description=In the CSS class, we float the image left, set its shape to be the same image, and then we set a margin of 30px.
|Code=.shape {    
	float: left;    
	shape-outside: url("http://openclipart.org/image/800px/svg_to_png/3201/nlyl_blue_circle.png");    
	shape-margin: 20px;    
}
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