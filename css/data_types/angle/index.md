{{Page_Title|Angle units}}
{{Flags
|High-level issues=Stub
|Editorial notes=(Stub to populate css/units tree)
}}
{{API_Name}}
{{Summary_Section|Specify angles used to rotate elements}}
{{Concept_Page
|Content=Four angle units are available:

* '''deg''' are degrees, of which there are 360 in a full circle.
* '''grad''' are grades, of which there are 400 in a full circle.
* '''rad''' are radians, of which there are 2&pi; in a full circle.
* '''turn''' are turns, of which one comprises a full circle.

Measurements may be positive or negative, and may extend past the
limit required to specify a full circle.

}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=.a[href] {
    display: block;
    transition: transform 0.25s;
    transform: rotateX(0deg);
}
a:hover {
    /* spin link 3 times & return to original orientation */
    transform: rotateX(1080deg);
}
}
}}
}}
{{Notes_Section
|Usage=__NOTES__
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Values and Units Module Level 3
|URL=http://www.w3.org/TR/css3-values/
|Status=Candidate Recommendation
}}
}}
{{See_Also_Section}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}