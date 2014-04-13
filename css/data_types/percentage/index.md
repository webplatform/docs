{{Page_Title|&lt;percentage&gt;}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{Summary_Section|The <code>&lt;percentage></code> CSS data type represents a number of measurement relative to another value.  It consists of a decimal or integer number immediately followed (without whitespace) by the percent sign, '''%'''.}}
{{Data_Type_Page
|Content=Percentages are expressed relative to other measurements, such as an element's dimensions, and can fall outside the 0%-100% range. What percentages are relative to is different for every property and is specified in the “Percentages” row of its definition.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=.box {
	width: 80%;
          /* relative to the parent container's
              content width */

	border-radius: 50%; 
          /* relative to this box's height or width;
              the computed value will be different
              in the x and y directions, creating an 
              ellipse. */

	font-size: 120%;
          /* relative to the inherited font size */
}
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Values and Units Module Level 3
|URL=http://www.w3.org/TR/css3-values/#percentage-value
|Status=W3C Candidate Recommendation
}}{{Related Specification
|Name=CSS 2.1
|URL=http://www.w3.org/TR/CSS21/about.html#percentage-wrt
|Status=W3C Recommendation
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