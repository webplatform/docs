{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Add compatibility.
|Checked_Out=No
|High-level issues=
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Sets the width of an element's four borders. This property can have from one to four values. This is a shorthand property for setting values simultaneously for [[css/properties/border-top-width|border-top-width]], [[css/properties/border-right-width|border-right-width]], [[css/properties/border-bottom-width|border-bottom-width]], and [[css/properties/border-left-width|border-left-width]].}}
{{CSS Property
|Initial value=medium, for all 4 values
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=An absolute length, for all 4 values; 0 if the border style is 'none' or 'hidden'
|Animatable=Yes
|CSS object model property=borderWidth
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=medium
|Description=Default.  
}}{{CSS Property Value
|Data Type=thin
|Description=Less than the default width.
}}{{CSS Property Value
|Data Type=thick
|Description=Greater than the default width.
}}{{CSS Property Value
|Data Type=<width>
|Description=Floating-point number, followed by an absolute units designator (<code>cm</code>, <code>mm</code>, <code>in</code>, <code>pt</code>, or <code>pc</code>) or a relative units designator (<code>em</code>, <code>ex</code>, or <code>px</code>). For more information about the supported length units, see [[http://www.w3.org/TR/css3-background/#the-border-width|CSS Values and Units Reference]].
}}{{CSS Property Value
|Data Type=<border-top-width> <border-right-width> <border-bottom-width> <border-left-width>
|Description=Shorthand syntax. See notes below.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=CSS border width values.
|Code=.medium {
  border-width: medium;
}

.thin {
  border-width: thin;
}

.thick {
  border-width: thick;
}

.width {
  border-width: 10px;
}

.various {
  border-width: thick medium thin 10px;
}
|LiveURL=http://code.webplatform.org/gist/733bf352438f33914fc0
}}
}}
{{Notes_Section
|Usage=* Up to four different widths can be specified, in the following order: top, right, bottom, left. 
* If one width is specified, it is used for all four sides. If two widths are specified, the first is used for the top and bottom borders, and the second is used for left and right borders. If three widths are specified, they are used for top, right/left, and bottom borders, respectively. If left is missing, it is the same as right; if bottom is missing, it is the same as top; if right is missing, it is the same as top.
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Level 3 - Backgrounds and Borders Module
|URL=http://www.w3.org/TR/css3-background/#the-border-width
|Status=Candidate Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Topic_clusters=Border
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}