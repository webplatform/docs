{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add description, compatibility.
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The <code>column-gap</code> property controls the width of the gap between columns in multi-column elements.}}
{{CSS Property
|Initial value=normal
|Applies to=multi-column elements
|Inherited=No
|Media=visual
|Computed value=absolute length or ‘normal’
|Animatable=Yes
|CSS object model property=columnGap
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=normal
|Description=Default. The width of the <code>normal</code> value is user-agent specific, but <code>1em</code> is suggested.
}}{{CSS Property Value
|Data Type=length
|Description=A floating-point number, followed by either an absolute units designator
(<code>cm</code>,
<code>mm</code>,
<code>in</code>,
<code>pt</code>,
or <code>pc</code>)
or a relative units designator
(<code>em</code>,
<code>ex</code>,
or <code>px</code>), that indicates the width of the gap between columns.
For more information about the supported length units,
see CSS Length Units Reference.


Negative values are not valid.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Makes as many 15em columns with a column-gap of 4em
|Code=/*
Makes as many 15em columns with a column-gap of 4em
*/

#columns {  
  /* Prefix free example below, use vendor prefixes where needed */
  column-width: 15em;
  column-gap: 4em;          
  column-rule: 1px solid green;
}
|LiveURL=http://code.webplatform.org/gist/5305647
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Multi-column Layout Module
|URL=http://www.w3.org/TR/css3-multicol/
|Status=Candidate Recommendation
}}
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
}}
}}
{{See_Also_Section
|Topic_clusters=Multi-Column
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}