{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Defines a two-dimensional transformation consisting of simultaneous skew transformations of the X and Y axes.  Not recommended and supported only for backwards compatibility; use a combination of ''skewX(angle)'', ''skewY(angle)'' and/or ''rotate(angle)'' instead.}}
{{CSS_Function}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The following code snippet is an example of the '''skew''' function in use. When applied to a square blue [[html/elements/div|'''div''']] element, it has the effect illustrated in the image. (The light-blue square indicates the original position of the transformed element.)
|Code=div {    
  transform: skew(42deg, -12deg);
}
|LiveURL=http://code.webplatform.org/gist/5305245
}}
}}
{{Notes_Section
|Import_Notes====Syntax===
'''skew'''
<code>(''
&lt;angle-x&gt;
'' , ''
&lt;angle-y&gt;
'')</code>
===Parameters===
;''angle-x'':The angle by which the element is skewed along the ''x''-axis. This value is expressed as a number followed by a supported angle unit.
;''angle-y'':The angle by which the element is skewed along the ''y''-axis. This value is expressed as a number followed by a supported angle unit.
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
|Topic_clusters=Transforms
|Manual_sections====Related pages (MSDN)===
*<code>Transform Functions</code>
*<code>[http://go.microsoft.com/fwlink/p/?LinkId{{=}}256246 Mathematical Description of Transform Functions]</code>
*<code>[http://go.microsoft.com/fwlink/?LinkID{{=}}240163 Hands On: 2D Transforms]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}