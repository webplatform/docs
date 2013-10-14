{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|CSS transforms allow elements styled with CSS to be transformed in two-dimensional or three-dimensional space. Using this property, elements can be translated, rotated, scaled, and skewed. The value list may consist of 2D and/or 3D transform values.}}
{{CSS Property
|Initial value=none
|Applies to=Transformable elements.
|Inherited=No
|Media=visual
|Computed value=As specified, but with relative lengths converted into absolute lengths.
|Animatable=Yes
|CSS percentages=Refer to the size of the element's bounding box.
|Values={{CSS Property Value
|Data Type=none
|Description=Specifies that no transform should be applied.
}}{{CSS Property Value
|Data Type=matrix(a, b, c, d, e, f)
|Description=Specifies a 2D transformation matrix in the form of a transformation matrix of the six values, a-f.
}}{{CSS Property Value
|Data Type=translate(tx, ty)
|Description=Specifies a 2D translation by the vector [tx, ty]. If ty is not specified, its value is assumed to be zero.
}}{{CSS Property Value
|Data Type=translateX(x)
|Description=Translates the element by the given amount along the X axis.
}}{{CSS Property Value
|Data Type=translateY(y)
|Description=Translates the element by the given amount along the Y axis.
}}{{CSS Property Value
|Data Type=scale(sx, sy)
|Description=Specifies a 2D scaling operation described by [sx, sy]. If sy is not specified, it is assumed to be equal to sx.
}}{{CSS Property Value
|Data Type=scaleX(sx)
|Description=Specifies a scale operation using the vector [sx, 1].
}}{{CSS Property Value
|Data Type=scaleY(sy)
|Description=Specifies a scale operation using the vector [1, sy].
}}{{CSS Property Value
|Data Type=rotate(a)
|Description=Specifies a 2D rotation by the specified angle about the origin of the element, as defined by the [[css/properties/transform-origin|transform-origin]] property.
}}{{CSS Property Value
|Data Type=skew(ax, ay)
|Description=Specifies a 2D skew by [ax,ay] for X and Y. If the second parameter is not provided, it is assumed to be zero.
}}{{CSS Property Value
|Data Type=skewX(ax)
|Description=Specifies a 2D skew transformation along the X axis by the given angle.
}}{{CSS Property Value
|Data Type=skewY(ay)
|Description=Specifies a 2D skew transformation along the Y axis by the given angle.
}}{{CSS Property Value
|Data Type=matrix3d(a, b, c, d, e, f, g, h, i, j, k, l, m, n, o, p)
|Description=Specifies a 3D transformation as a 4x4 homogeneous matrix of 16 values in column-major order.
}}{{CSS Property Value
|Data Type=translate3d(tx, ty, tz)
|Description=Specifies a 3D translation by the vector [tx,ty,tz] in the X, Y, and Z directions.
}}{{CSS Property Value
|Data Type=translateZ(tz)
|Description=Specifies a 3D translation by the vector [0,0,tz] in the Z direction.
}}{{CSS Property Value
|Data Type=scale3d(sx, sy, sz)
|Description=Specifies a 3D scale operation by the [sx,sy,sz] scaling vector described by the three parameters.
}}{{CSS Property Value
|Data Type=scaleZ(sz)
|Description=Specifies a 3D scale operation by the scaling vector [1,1,sz].
}}{{CSS Property Value
|Data Type=rotate3d(x, y, z, a)
|Description=Specifies a 3D rotation by the angle specified in last parameter about the [x,y,z] direction vector described by the first three parameters.
}}{{CSS Property Value
|Data Type=rotateX(ax)
|Description=Specifies a 3D rotation by the angle specified in the X direction. Equivalent to <code>rotate3d(1, 0, 0, ax)</code>.
}}{{CSS Property Value
|Data Type=rotateY(ay)
|Description=Specifies a 3D rotation by the angle specified in the Y direction. Equivalent to <code>rotate3d(0, 1, 0, ay)</code>.
}}{{CSS Property Value
|Data Type=rotateZ(az)
|Description=Specifies a 3D rotation by the angle specified in the Z direction. Equivalent to <code>rotate3d(0, 0, 1, az)</code>.
}}{{CSS Property Value
|Data Type=perspective(p)
|Description=Specifies a perspective projection matrix, which scales points in the X and Y directions based on their Z value. Thus, points with positive Z values are scaled away from the origin, and those with negative Z values are scaked toward the origin.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Translate the object by 150 pixels along the x and y axes
|Code=.matrix {
 	-webkit-transform:  matrix(1, 0, 0, 1, 150, 150);
 	-o-transform:  matrix(1, 0, 0, 1, 150, 150);
 	-moz-transform:  matrix(1, 0, 0, 1, 150, 150);
 	-ms-transform:  matrix(1, 0, 0, 1, 150, 150);
 	transform:  matrix(1, 0, 0, 1, 150, 150);
 	
 	width: 10em;
 	height: 10em;
 	background: #eee;
 }
|LiveURL=http://dabblet.com/gist/4740688
}}{{Single Example
|Language=CSS
|Description=Rotate the object by 40deg
|Code=.rotate {
	-ms-transform: rotate(40deg);
	-webkit-transform: rotate(40deg);
	-o-transform: rotate(40deg);
	-moz-transform: rotate(40deg);
	transform: rotate(40deg);
	
	width: 10em;
	height: 10em;
	background-color: red;
}
|LiveURL=http://dabblet.com/gist/4744780
}}{{Single Example
|Language=CSS
|Description=Scales the element by the factor of 3 on the x axis and by the factor of 0.5 by the y axis.
|Code=.scale {
	-ms-transform: scale(3, 0.5);
	-webkit-transform: scale(3, 0.5);
	-o-transform: scale(3, 0.5);
	-moz-transform: scale(3, 0.5);
	transform: scale(3, 0.5);

	width: 10em;
	height: 10em;
	background: green;
}
|LiveURL=http://dabblet.com/gist/4745494
}}{{Single Example
|Language=CSS
|Description=Rotate the object by 40deg along the X axis.
|Code=.rotateX {
	-ms-transform: rotateX(40deg);
	-webkit-transform: rotateX(40deg);
	-o-transform: rotateX(40deg);
	-moz-transform: rotateX(40deg);
	transform: rotateX(40deg);
	
	width: 10em;
	height: 10em;
	background-color: blue;
}
|LiveURL=http://dabblet.com/gist/6123429
}}
}}
{{Notes_Section
|Notes=Any value other than "none" results in the creation of both a stacking context and a containing block. The containing block is for fixed positioned descendants.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Transforms Module Level 3
|URL=http://www.w3.org/TR/css3-transforms
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
|External_links=Cross Browser CSS Transforms – Even in IE http://www.useragentman.com/blog/2010/03/09/cross-browser-css-transforms-even-in-ie/
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/transform transform
|MSDN_link=
|HTML5Rocks_link=
}}
[[file:transform_example.png|alt Example showing translate, scale and rotate step by step]]