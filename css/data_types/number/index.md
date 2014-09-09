{{Page_Title|&lt;number&gt;}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{Summary_Section|The <code>&lt;number></code> CSS data type represents positive or negative decimal or integer values.}}
{{Data_Type_Page
|Content=Numbers in the [http://www.w3.org/TR/css3-values/#numbers CSS definition] can accept ordinary decimal numbers: a series of digits optionally followed by a decimal point ('''.''') and more digits, with an optional exponent component (the latter is usually referred to as a scientific notation).

===Notes===
*Due to being a new feature of the CSS Syntax module, the browser support for scientific notations (the optional exponent component) varies and therefore, it should be used with caution. Supporting browsers include Internet Explorer 11, Firefox 29 and Chrome 39.
*Before the CSS 3 Syntax module was introduced, numbers in CSS differed from the [http://www.w3.org/TR/SVG11/types.html#DataTypeNumber SVG definition] which always allowed for numbers in attribute properties to be specified using scientific notation (such as '''1.3e-5''' for '''0.000013''').  If an SVG presentational attribute were specified using CSS styles, it must have conformed to the CSS data type.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=
|Code=.box {
  /* Flip & enlarge */
  transform: scale(-1.2); 
}
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Values and Units Module Level 3
|URL=http://www.w3.org/TR/css3-values/#numbers
|Status=W3C Candidate Recommendation
|Relevant_changes=
}}{{Related Specification
|Name=CSS 2.1
|URL=http://www.w3.org/TR/CSS21/syndata.html#numbers
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related Specification
|Name=CSS Syntax Module Level 3
|URL=http://www.w3.org/TR/css-syntax-3/#number-token-diagram
|Status=W3C Candidate Recommendation
|Relevant_changes=Scientific notation is now supported.
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
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}