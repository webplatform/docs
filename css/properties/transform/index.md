{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The CSS transform property lets you modify the coordinate space of the CSS visual formatting model. Using it, elements can be translated, rotated, scaled, and skewed according to the values set.

If the property has a value different than none, a stacking context will be created. In that case the object will act as a containing block for position: fixed elements that it contains.
}}
{{CSS Property
|Initial value=none
|Applies to=any transformable element
|Inherited=No
|Media=visual
|Computed value=?
|Animatable=Yes
|Values={{CSS Property Value
|Data Type=matrix(1.0, 2.0, 3.0, 4.0, 5.0, 6.0)
|Description=Specifies a 2D transformation matrix comprised of the specified six values. This is the equivalent to applying the transformation matrix [a b c d tx ty].
}}{{CSS Property Value
|Data Type=translate(12px, 50%)
|Description=Specifies a 2D translation by the vector [tx, ty]. If ty isn't specified, its value is assumed to be zero.
}}{{CSS Property Value
|Data Type=translateX(2em)
|Description=Translates the element by the given amount along the X axis.
}}{{CSS Property Value
|Data Type=translateY(50px)
|Description=Translates the element by the given amount along the Y axis.
}}{{CSS Property Value
|Data Type=scale(2, 0.5)
|Description=Specifies a 2D scaling operation described by [sx, sy]. If sy isn't specified, it is assumed to be equal to sx.
}}{{CSS Property Value
|Data Type=scaleX(3)
|Description=Specifies a scale operation using the vector [sx, 1].
}}{{CSS Property Value
|Data Type=scaleY(0.5)
|Description=Specifies a scale operation using the vector [1, sy].
}}{{CSS Property Value
|Data Type=rotate(20deg)
|Description=Rotates the element clockwise around its origin (as specified by the transform-origin property) by the specified angle. 
}}{{CSS Property Value
|Data Type=none
|Description=Specifies that no transform should be applied.
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
|LiveURL=http://dabblet.com/gist/4740525
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/CSS/transform transform]
|MSDN_link=
|HTML5Rocks_link=
}}