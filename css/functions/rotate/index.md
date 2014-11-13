{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Rotates an element clockwise around its origin (as specified by the '''transform-origin''' property) by the specified angle. The operation corresponds to the matrix [cos(angle) sin(angle) -sin(angle) cos(angle) 0 0].}}
{{CSS_Function
|Content=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The following code snippet is an example of the rotate function in use.
|Code=div {    
  transform: rotate(33.3deg);
}
|LiveURL=http://code.webplatform.org/gist/10500f11ec6168049ba5
}}
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes====Syntax===
'''rotate'''
<code>(''
&lt;angle&gt;
'')</code>
===Parameters===
;''angle'':The angle by which the element is rotated about its origin. If not specified otherwise, the element rotates around its center. The origin can be specified with the [http://docs.webplatform.org/wiki/css/properties/transform-origin transform-origin property].  This value is expressed as an integer or decimal number followed by a supported angle unit.
===Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkID{{=}}223145 CSS Transforms Module, Level 3], Section 13.1
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Transforms Module Level 3
|URL=http://go.microsoft.com/fwlink/p/?LinkID=223145
|Status=Working Draft
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
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
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}