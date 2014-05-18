{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|This property specifies how nested elements are rendered in 3D space relative to their parent.}}
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
|Description=Child elements will not preserve their 3D position before applying a transform.
}}{{CSS Property Value
|Data Type=preserve-3d
|Description=Child elements will preserve their 3D position before applying a transform.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/* The transformed child div (green) will preserve 
   the 3D position applied by the parent div (blue) 
   before applying its own transform */
#blue {
width: 10em;
height: 10em;
background-color: blue;
transform: rotateY(60deg);
transform-style: preserve-3d;
}

#green {
margin-left: 30px;
width: 10em;
height: 10em;
background-color: green;
transform: rotateY(60deg);
}
|LiveURL=http://code.webplatform.org/gist/6995453
}}
}}
{{Notes_Section
|Notes=This property is only applied to child elements that have a [[css/transforms/transform|transform]] specified.
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