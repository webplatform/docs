{{Page_Title}}
{{Flags
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The <code>padding</code> optional CSS property sets the required padding space on one to four sides of an element. The padding area is the space between an element and its border. Negative values are not allowed but decimal values are permitted.  The element size is treated as fixed, and the content of the element shifts toward the center as padding is increased.

The <code>padding</code> property is a shorthand to avoid setting each side separately ([[css/properties/padding-top|padding-top]], [[css/properties/padding-right|padding-right]], [[css/properties/padding-bottom|padding-bottom]], [[css/properties/padding-left|padding-left]]).
}}
{{CSS Property
|Initial value=0
|Applies to=all elements (except table-*-group, table-row and table-column, br)
|Inherited=No
|Media=visual
|Computed value=the percentage or the absolute length
|Animatable=Yes
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
|Description=Padding set at 5% for all 4 sides.
|Code=padding: 5% 5% 5% 5%; 
      /*  top, right, bottom, and left padding set at 5%   */
|LiveURL=http://code.webplatform.org/gist/5842631
}}{{Single Example
|Language=CSS
|Description=The padding style has three values. The left padding value is the inferred by the right padding value.
|Code=padding: 10px 3% 20px;    
      /*  top 10px padding          */
      /*  left and right 3% padding */
      /*  bottom 20px padding       */
}}{{Single Example
|Language=CSS
|Description=The padding style has two values. The left padding value is the inferred by the right padding value.  The bottom value is inferred by the top value.
|Code=padding: 10px 20%;  
      /*  top and bottom 10px padding  */
       /*  left and right 20% padding  */
}}{{Single Example
|Language=CSS
|Description=The padding style has one value. All the values are inferred to be equal to the top padding value of 10 px.
|Code=padding: 10px; 
       /* on all sides 10px padding */
}}{{Single Example
|Language=CSS
|Description=The padding style has one value. All the values are inferred to be equal to the top padding value of 20%.
|Code=padding: 10px; 
       /* on all sides 20% padding */
}}
}}
{{Notes_Section
|Notes=This is a composite property that specifies up to four padding values, in the following order: top, right, bottom, left. If one width value is specified, it is used for all four sides. If two width values are specified, the first is used for the top and bottom borders, and the second is used for left and right borders. If three width values are specified, they are used for top, right/left, and bottom borders, respectively. Negative values are not allowed.

As of Microsoft Internet Explorer 5.5, this property applies to inline elements.  With earlier versions of  Windows Internet Explorer, inline elements must have an '''absolute''' [[css/properties/position|'''position''']] or layout to use this property. 

Element layout is set by providing a value for the [[css/properties/height|'''height''']] property or the [[css/properties/width|'''width''']] property.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=CSS Layout, Box Model
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|HTML5Rocks_link=
}}