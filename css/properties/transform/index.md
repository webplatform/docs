{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|CSS transforms allows elements styled with CSS to be transformed in two-dimensional or three-dimensional space.

The CSS transform property lets you modify the coordinate space of the CSS visual formatting model. Using it, elements can be translated, rotated, scaled, and skewed according to the values set.

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
|Data Type=none
|Description=Specifies that no transform should be applied.
}}{{CSS Property Value
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
|Description=Rotates the element clockwise around its origin (as specified by the transform-origin property) by the specified [[css/units/angle|angle]].
}}{{CSS Property Value
|Data Type=skewX(40deg)
|Description=Specifies a 2D skew transformation along the X axis by the given [[css/units/angle|angle]].
}}{{CSS Property Value
|Data Type=skewY(0.25turn)
|Description=Specifies a 2D skew transformation along the Y axis by the given [[css/units/angle|angle]].
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
|Description=Rotate the object by 20deg
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
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=Basic Support
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=1.0
|Firefox_supported=Yes
|Firefox_version=16
|Firefox_prefixed_supported=Yes
|Firefox_prefixed_version=3.5
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=Yes
|Internet_explorer_prefixed_version=9.0
|Opera_supported=Yes
|Opera_version=12.1
|Opera_prefixed_supported=Yes
|Opera_prefixed_version=10.5
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Yes
|Safari_prefixed_version=3.1
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Feature=Basic Support
|Android_supported=Unknown
|Android_version=
|Android_prefixed_supported=Yes
|Android_prefixed_version=2.1
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Yes
|Blackberry_prefixed_version=7.0
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Yes
|Chrome_mobile_prefixed_version=18.0
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=16
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=11.0
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Unknown
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Yes
|Safari_mobile_prefixed_version=3.1
}}
|Notes_rows=
}}
{{See_Also_Section
|External_links=Cross Browser CSS Transforms – even in IE http://www.useragentman.com/blog/2010/03/09/cross-browser-css-transforms-even-in-ie/
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/CSS/transform transform]
|MSDN_link=
|HTML5Rocks_link=
}}
[[file:transform_example.png|alt Example showing translate, scale and rotate step by step]]