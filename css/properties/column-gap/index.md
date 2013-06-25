{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
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
|Description=This example demonstrates how you can eliminate those nasty white-spaces in between your columns in your page for maximum content effect.
|Code=section.newspaper {
    -webkit-column-count: 5;
    -moz-column-count: 5;
    column-count: 5;
 
    -webkit-column-gap: 0;
    -moz-column-gap: 0;
    column-gap: 0;
}
}}{{Single Example
|Language=CSS
|Description=Makes as many columns that are 15em as the browser lets
you. Put a green line between the columns and pad the 
content
|Code=#column3 {
    column-width: 15em;
    column-gap: 2em;          
    column-rule: 4px solid green;
    padding: 5px;
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
|Notes_rows=
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