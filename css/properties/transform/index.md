{{Page_Title}}
{{Flags

}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The CSS transform property lets you modify the coordinate space of the CSS visual formatting model. Using it, elements can be translated, rotated, scaled, and skewed according to the values set.

If the property has a value different than none, a stacking context will be created. In that case the object will act as a containing block for position: fixed elements that it contains.}}
{{CSS Property
|Initial value=non
|Applies to=any transformable element
|Inherited=No
|Media=visual
|Computed value=?
|Animatable=Yes in some browsers
|Values={{CSS Property Value
|Data Type=none
|Description=Specifies that no transform should be applied.}}
}}
{{CSS Property Value
|Data Type=matrix(1.0, 2.0, 3.0, 4.0, 5.0, 6.0)
|Description=Specifies a 2D transformation matrix comprised of the specified six values. This is the equivalent to applying the transformation matrix [a b c d tx ty].}}
{{CSS Property Value
|Data Type=translate(12px, 50%)
|Description=Specifies a 2D translation by the vector [tx, ty]. If ty isn't specified, its value is assumed to be zero.}}
}}
{{Examples_Section
|Not_required=No
|Examples=
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