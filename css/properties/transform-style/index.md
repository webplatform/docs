{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|This property specifies how nested elements are rendered in 3D space.}}
{{CSS Property
|Initial value=flat
|Applies to=Transformable elements.
|Inherited=No
|Media=visual
|Computed value=As specified.
|Animatable=No
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=flat
|Description=Child elements will not preserve their 3D position.
}}{{CSS Property Value
|Data Type=preserve-3d
|Description=Child elements will preserve their 3D position.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/* Transformed child elements will preserve the 3D transformation */
div {
    transform: rotateY(60deg);
    transform-style: preserve-3d;
    -webkit-transform: rotateY(60deg);
    -webkit-transform-style: preserve-3d;
}
}}
}}
{{Notes_Section
|Notes=This property does not affect how the object is rendered.
This property is only applied to child elements that have a [[css/transforms/transform|transform]] specified.
The  object is the projection plane for the child elements.
Child elements cannot intersect in <code>flat</code> mode.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Transforms
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
{{See_Also_Section}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}