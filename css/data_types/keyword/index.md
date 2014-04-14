{{Page_Title|CSS keywords}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|Mixed}}
{{Summary_Section|Many CSS properties have specific keywords which may be used as values; in addition, the keywords '''initial''' and '''inherit''' may be used as the value of any CSS property.}}
{{Data_Type_Page
|Content=The keywords relevant to a specific  CSS property are defined in its [[css/properties | property page]].  All keywords meet the requirements of [[css/data_types/custom_ident | CSS identifiers]], and are case sensitive.  Keywords should never be quoted.

===CSS-wide keywords===

Certain keywords can be used for any CSS property value:

* '''inherit''' copies the value of the property in effect for the element's parent.

* '''initial''' represents the initial (or default) value for the property, over-riding any values set earlier in the cascade; initial values are defined on each property's definition; it is not supported in Internet Explorer.

* '''unset''' is equivalent to '''inherit''' if the property is normally inherited, or '''initial''' otherwise; it is not currently supported in most browsers (except Firefox).


}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=body{
    height:100%;
	background-image:radial-gradient(ellipse , yellow, orange 30%);
	text-align:center; 
	/* a property-specific keyword */
}
h1 {
   background-image:inherit; 
   /* inherit a not-normally inherited property 
      (note that there is a second gradient that fits the
      heading box)
   */
}
p {
   text-align:initial; 
   /* over-ride an inheritied property,
      if your browser supports the initial keyword */ 
}
a {
  color: inherit !important; 
  /* over-ride a user stylesheet property */

  text-decoration: unset; 
  /* over-ride a user stylesheet property,
     if your browser supports the unset keyword */
}
|LiveURL=http://code.webplatform.org/gist/10615256
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Cascading and Inheritance Level 3
|URL=http://www.w3.org/TR/css3-cascade/#inherit-initial
|Status=W3C Candidate Recommendation
|Relevant_changes=Defines the <code>unset</code> keyword.
}}{{Related Specification
|Name=CSS Values and Units Module Level 3
|URL=http://www.w3.org/TR/css3-values/#keywords
|Status=W3C Candidate Recommendation
|Relevant_changes=Defines the <code>initial</code> keyword.
}}{{Related Specification
|Name=CSS 2.1
|URL=http://www.w3.org/TR/CSS21/cascade.html#value-def-inherit
|Status=W3C Recommendation
|Relevant_changes=Defines the <code>inherit</code> keyword.
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