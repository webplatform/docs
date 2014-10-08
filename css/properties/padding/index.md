{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The <code>padding</code> optional CSS property sets the required padding space on one to four sides of an element. The padding area is the space between an element and its border. Negative values are not allowed but decimal values are permitted.  The element size is treated as fixed, and the content of the element shifts toward the center as padding is increased.

The <code>padding</code> property is a shorthand to avoid setting each side separately ([[css/properties/padding-top|padding-top]], [[css/properties/padding-right|padding-right]], [[css/properties/padding-bottom|padding-bottom]], [[css/properties/padding-left|padding-left]]).
}}
{{CSS Property
|Initial value=browser-dependent
|Applies to=all elements (except table-*-group, table-row and table-column, br)
|Inherited=No
|Media=visual
|Computed value=the percentage or the absolute length
|Animatable=Yes
|CSS object model property=
|CSS percentages=relative to the 'width' of the containing block
|Values={{CSS Property Value
|Data Type=length
|Description=Specifies a non-negative fixed width defined in pixels, pt, em, etc. . See [[css/data_types/length|length]] for details.
}}{{CSS Property Value
|Data Type=percentage
|Description=Calculated using the dimensions of the containing block or element.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Padding set at 10% for all 4 sides.
|Code=padding: 10% 10% 10% 10%; 
      /*  top, right, bottom, and left padding set at 10%   */
|LiveURL=http://code.webplatform.org/gist/5842631
}}{{Single Example
|Language=CSS
|Description=The padding style has three values. The left padding value is the inferred by the right padding value.
|Code=padding: 10px 3% 20px;    
      /*  top 10px padding          */
      /*  left and right 3% padding */
      /*  bottom 20px padding       */
|LiveURL=
}}{{Single Example
|Language=CSS
|Description=The padding style has two values. The left padding value is the inferred by the right padding value.  The bottom value is inferred by the top value.
|Code=padding: 10px 20%;  
      /*  top and bottom 10px padding  */
       /*  left and right 20% padding  */
|LiveURL=
}}{{Single Example
|Language=CSS
|Description=The padding style has one value. All the values are inferred to be equal to the top padding value of 10 px.
|Code=padding: 10px; 
       /* on all sides 10px padding */
|LiveURL=
}}{{Single Example
|Language=CSS
|Description=The padding style has one value. All the values are inferred to be equal to the top padding value of 20%.
|Code=padding: 20%; 
       /* on all sides 20% padding */
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=This is a composite property that specifies up to four padding values, in the following order: top, right, bottom, left. If one width value is specified, it is used for all four sides. If two width values are specified, the first is used for the top and bottom borders, and the second is used for left and right borders. If three width values are specified, they are used for top, right/left, and bottom borders, respectively. Negative values are not allowed.

As of Microsoft Internet Explorer 5.5, this property applies to inline elements.  With earlier versions of  Windows Internet Explorer, inline elements must have an '''absolute''' [[css/properties/position|'''position''']] or layout to use this property. 

Element layout is set by providing a value for the [[css/properties/height|'''height''']] property or the [[css/properties/width|'''width''']] property.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS basic box model
|URL=http://www.w3.org/TR/css3-box/
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related Specification
|Name=CSS 2.1, 8 Box model
|URL=http://www.w3.org/TR/CSS21/box.html#propdef-padding
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}