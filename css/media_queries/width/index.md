{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add values, syntax, description,, compatibility.
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The ‘width’ media feature describes the width of the targeted display area of the output device. For continuous media, this is the width of the viewport (as described by CSS2, section 9.1.1 [CSS21]) including the size of a rendered scroll bar (if any). For paged media, this is the width of the page box (as described by CSS2, section 13.2 [CSS21]).}}
{{CSS_Media_Feature
|Content===Description==
The width media query returns the width of the layout viewport, also called the initial containing block. This is equal to the default width of the html element. Thus, it tells you how much space the browser allows your CSS layout to take.

The width media query is one of the two vital ingredients of responsive web design; the other one is the [[tutorials/mobile_viewport|meta viewport tag]]. The width media query is very reliable across browsers, and using it will not raise compatibility issues.

The width media query is always, in all browsers, equal to document.documentElement.clientWidth.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=@media (width:400px){
   /*This code will only be run if the width of the viewport is exactly 400px*/
}
@media (min-width:400px){
   /*This code will only be run if the width of the viewport is at least 400px*/
}
@media (max-width:400px){
   /*This code will only be run if the width of the viewport is at most 400px*/
}
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Media Queries Level 4
|URL=http://www.w3.org/TR/mediaqueries-4/
|Status=Working Draft
}}{{Related Specification
|Name=Media Queries
|URL=http://www.w3.org/TR/css3-mediaqueries/
|Status=Recommendation
}}
}}
{{See_Also_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}



@media screen and (min-width: 400px) and (max-width: 700px) { … }