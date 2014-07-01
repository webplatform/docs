{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=Can be used as-is, though out of style with the rest of the function pages as it doesn't list the others in related links.
|Checked_Out=No
|High-level issues=Needs Review
|Content=Incomplete
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The <b>calc()</b> function can be used anywhere in a length is required by a CSS properties. calc() allows mathematical expressions with addition (‘+’), subtraction (‘-’), multiplication (‘*’), and division (‘/’) to be used as component values. The values themselves can be a mixture of percentages, integers, numbers, lengths such as em or cm, angles or even time values ( seconds, milliseconds). Calc is useful for computing certain values that are not known at the development time or to set formulated values rather that arbitrary ones.}}
{{CSS_Function}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=This is an example of how can you use <b>calc</b> in CSS
|Code=/* CSS calc function example */
 
.header {
     position:relative;
     margin: 0px auto;
     width: 80%; /* fallback for browsers without support for calc() */
     width: calc(100% - 100px); /* CSS3 compliant implementation; Firefox 16 and IE 9, and above */
     border: solid black 1px;
     box-shadow: 5px 5px #999;
     margin-top: 40px;
     padding: 10px;
     text-align: center;
}
 
.header:hover {
     width: calc(100% / 3 - 2 * 1em); /* complex calculation on hover */
     width: 25%; /* fallback */
}
|LiveURL=http://code.webplatform.org/gist/d3322a08edaaaef9adaf
}}
}}
{{Notes_Section
|Notes=If you divide by zero it will cause an error in the HTML parser. Also the return value that will be computed must comply within the range of the relevant CSS target. For example width or height cannot be negative so it will be reverted to 0;
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C CSS Values and Units Module Level 3: Mathematical Expressions: "calc"
|URL=http://www.w3.org/TR/css3-values/#calc-notation
|Status=Candidate Reccomendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=26
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=22
|Firefox_supported=Yes
|Firefox_version=16
|Firefox_prefixed_supported=Yes
|Firefox_prefixed_version=4
|Internet_explorer_supported=Yes
|Internet_explorer_version=9
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=Yes
|Safari_prefixed_version=6
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=No
|Android_version=
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=No
|Blackberry_version=
|Blackberry_prefixed_supported=Yes
|Blackberry_prefixed_version=10.0
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=26
|Chrome_mobile_prefixed_supported=Yes
|Chrome_mobile_prefixed_version=25
|Firefox_mobile_supported=Yes
|Firefox_mobile_prefixed_supported=Yes
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Yes
|Safari_mobile_prefixed_version=6
}}
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