{{Page_Title|&lt;angle&gt;}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{Summary_Section|The <code>&lt;angle></code> CSS data type describes an amount of rotation; it is expressed with a number followed (without whitespace) by one of the recognized angle unit abbreviations.}}
{{Data_Type_Page
|Content=Four angle units are available:

* '''deg''' are degrees, of which there are 360 in a full circle.
* '''grad''' are grades, of which there are 400 in a full circle.
* '''rad''' are radians, of which there are 2&pi; in a full circle.
* '''turn''' are turns, of which one comprises a full circle.

Measurements may be positive or negative, and may extend past the
limit required to specify a full circle.

If using Javascript to set or manipulate styles requiring angle measurements, it is worth mentioning that the trigonometric [[concepts/programming/javascript/core_objects#Math_Object|Math functions]] use radians for angles.
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
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Values and Units Module Level 3
|URL=http://www.w3.org/TR/css3-values/
|Status=Candidate Recommendation
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
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}
{{API_Name}}








}




}