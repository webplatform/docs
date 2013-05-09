{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Sets the width of an element's top border. To set all four borders, use the [[css/properties/border-width|border-width]] shorthand property which sets the values simultaneously for [[css/properties/border-top-width|border-top-width]], [[css/properties/border-right-width|border-right-width]], [[css/properties/border-bottom-width|border-bottom-width]], and [[css/properties/border-left-width|border-left-width]].}}
{{CSS Property
|Initial value=medium
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=An absolute length; 0 if the border style is 'none' or 'hidden'
|Animatable=No
|CSS object model property=borderTopWidth
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
|Description=Floating-point number, followed by an absolute units designator (<code>cm</code>, <code>mm</code>, <code>in</code>, <code>pt</code>, or <code>pc</code>) or a relative units designator (<code>em</code>, <code>ex</code>, or <code>px</code>). For more information about the supported length units, see CSS Values and Units Reference.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=CSS border width values.
|Code=.medium {
  border-top-width: medium;
}

.thin {
  border-top-width: thin;
}

.thick {
  border-top-width: thick;
}

.width {
  border-top-width: 10px;
}
|LiveURL=http://code.webplatform.org/gist/5550302
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C CSS Backgrounds and Borders Module Level 3
|URL=http://www.w3.org/TR/css3-background/#border-width
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
{{See_Also_Section
|Topic_clusters=Border
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}