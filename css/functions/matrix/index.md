{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Missing image link in red.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|<p>Defines a two dimentional transofmation in matrix format_ That is a function  <b>matrix(a,b,c,d,e,f)</b> which holds 6 parameters as numbers each one controlling one tranformation factor_ In fact, matrix combines all the CSS tranformation functions (translate,skew etc) in one command_ For example the new position of a point <b>(x,y)</b> will be such that:  <pre>newX=a*x + c*y + e</pre> and <pre>newY = b*x + d*y + f</pre>  </p>
}}
{{CSS_Function}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=-webkit-transform: matrix(1, 0, 0.5, 1, 10, 0);
-o-transform: matrix(1, 0, 0.5, 1, 10, 0);
transform: matrix(1, 0, 0.5, 1, 10, 0);
|LiveURL=http://jsfiddle.net/denbuzze/J2CLV/1/
}}
}}
{{Notes_Section
|Notes====Remarks===
A 2-D 3×2 matrix with six parameters ''a'', ''b'', ''c'', ''d'', ''e'', and ''f'' is equivalent to the following transformation matrix: [[Image:2dmatrix.png]] For more information about transformation matrices, see [http://go.microsoft.com/fwlink/p/?LinkId{{=}}256246 Mathematical Description of Transform Functions], in the [http://go.microsoft.com/fwlink/?LinkID{{=}}223145 CSS3 Transforms] specification.
|Import_Notes====Syntax===
'''matrix'''
<code>(''
&lt;number&gt;
'' , ''
&lt;number&gt;
'' , ''
&lt;number&gt;
'' , ''
&lt;number&gt;
'' , ''
&lt;number&gt;
'' , ''
&lt;number&gt;
'')</code>
===Parameters===
;''number'':A matrix value.
===Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkID{{=}}223145 CSS Transforms Module, Level 3], Section 13.1


===Requirements===
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
*<code>Direct3D: Matrices</code>
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