{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Specifies the width of columns in multi-column elements.}}
{{CSS Property
|Initial value=auto
|Applies to=non-replaced block-level elements (except table elements), table cells, and inline-block elements
|Inherited=No
|Media=visual
|Computed value=the absolute length, zero or larger
|Animatable=Yes
|CSS object model property=columnWidth
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=length
|Description=A floating-point number, followed by either an absolute units designator
(<code>cm</code>,
<code>mm</code>,
<code>in</code>,
<code>pt</code>,
or <code>pc</code>)
or a relative units designator
(<code>rem</code>, <code>em</code>,
<code>ex</code>,
or <code>px</code>), that indicates the optimal width.
For more information about the supported length units,
see CSS Length Units Reference.
}}{{CSS Property Value
|Data Type=auto
|Description=Default. The optimal column width is determined through other property values of the multi-column element, such as [[css/properties/column-count|'''columnCount''']].
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Makes as many columns that are 100px as there is space in the browser.
|Code=/*
Makes as many columns that are 100px as there is space in the browser.
*/

#column {
  /* Prefix free example below, use vendor prefixes where needed */
  column-width: 100px;
}
|LiveURL=http://code.webplatform.org/gist/5305475
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
The actual column width may vary from the value specified due to available space.
To ensure that the exact value specified for this property is used, all property values of the multi-column element that pertain to length (such as width, column-width, column-gap, and column-rule-width) must be specified.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Multi-column Layout Module
|URL=http://www.w3.org/TR/css3-multicol/
|Status=Candidate Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Topic_clusters=Multi-Column
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
|Notes_rows={{Compatibility Notes Row
|Browser=Chrome
|Note=Requires -webkit- prefix
}}{{Compatibility Notes Row
|Browser=Safari
|Note=Requires -webkit- prefix
}}{{Compatibility Notes Row
|Browser=Opera
|Version=14–Current
|Note=Requires -webkit- prefix
}}{{Compatibility Notes Row
|Browser=Firefox
|Note=Requires -moz- prefix
}}{{Compatibility Notes Row
|Browser=IE
|Version=10
}}
}}