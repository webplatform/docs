{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_At_Rule
|Content=
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The default namespace is applied to names that do not have an explicit namespace component. The following rule declares a default namespace.
|LiveURL=
|Code=
@namespace "http://www.w3.org/1999/xhtml";
}}
{{Single_Example
|Description=If  you declare an '''@namespace''' rule  with a prefix,  you can use the prefix  in namespace-qualified names. For example,  consider  the following namespace declaration for a namespace <code>prfx</code>.
|LiveURL=
|Code=
@namespace prfx "http://prfx.contoso.com";
}}
{{Single_Example
|Description=Based on the previous declaration, the following selector matches <code>E</code> elements in the namespace  that  the <code>prfx</code> prefix refers to.
|LiveURL=
|Code=
prfx{{!}}E
}}
{{Single_Example
|Description=The following code  example creates  two namespace prefixes. First, <code>p</code> elements in any namespace are colored red. Any <code>p</code> elements in the  <code>prfx</code>  namespace are then recolored blue, and <code>p</code> elements in the  <code>msft</code>  namespace are recolored green.
|LiveURL=
|Code=
@namespace prfx "http://prfx.contoso.com";
@namespace msft "http://msft.example.com";
 p {background-color:red;}
prfx{{!}}p {background-color:blue;}
msft{{!}}p {background-color:green;}
}}
{{Single_Example
|Description=The following code  example styles a SVG element.  By using the namespace and declaration from this example, all circles  that are created with SVG  are  given a red fill.
|LiveURL=
|Code=
@namespace svg "http://www.w3.org/2000/svg";
svg{{!}}circle {fill:red;}
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''@namespace''' rule  was  introduced in Windows Internet Explorer 9.
The scope of an '''@namespace''' rule is the style sheet  that  it is declared in.  You must declare an '''@namespace''' rule  after any [[css/atrules/@charset|'''@charset''']] or [[css/atrules/@import|'''@import''']] rules.
|Import_Notes=
===Syntax===
<code>'''@namespace '''''prfx'''''?''' ''sUrl''</code>
===Parameters===
;''prfx'':Optional. A '''String'''  value that specifies a namespace prefix.
;''sUrl'':A URL '''String'''value that specifies a namespace name.
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199783 Selectors Level 3], Section 3


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>Reference</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[css/cssom/styleSheet|styleSheet]]</code>
|Topic_clusters=Syntax
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}