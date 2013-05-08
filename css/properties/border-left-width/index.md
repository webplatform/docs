{{Page_Title}}
{{Flags
|Content=Not Neutral, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Sets the width of an element's left border.}}
{{CSS Property
|Initial value=medium
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=absolute length; 0 if the border style is 'none' or 'hidden'
|Animatable=No
|CSS object model property=borderLeftWidth
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
|Description=The following example sets the left border width of the <code>div</code> with a class of <code>box</code> to 0.8em.
|Code=.box {
  /* A border needs to be specified in order for the border-left-width to take effect. */
  border: 6px solid #444;
  
  /* The border-left-width can be specified in px, em, cm, mm, in etc.*/
  border-left-width: 0.8em;
}
|LiveURL=http://code.webplatform.org/gist/5535147
}}
}}
{{Notes_Section
|Notes=
As of Microsoft Internet Explorer 5.5, this property applies to inline elements.  With earlier versions of  Windows Internet Explorer, inline elements must have an '''absolute''' [[css/properties/position|'''position''']] or layout to use this property. Element layout is set by providing a value for the [[css/properties/height|'''height''']] property or the [[css/properties/width|'''width''']] property.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Backgrounds and Borders Module Level 3
|URL=http://www.w3.org/TR/css3-background/#the-border-width
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
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Reference</code>
*<code>[[css/properties/border|border]]</code>
*<code>[[css/properties/border-width|border-width]]</code>
*<code>Other Resources</code>
*<code>CSS Enhancements in Internet Explorer 6</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}