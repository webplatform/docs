{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Declares the default namespace and binds a namespace to a namespace prefix.}}
{{CSS_At_Rule}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The default namespace is applied to names that do not have an explicit namespace component. The following rule declares a default namespace.
|Code=@namespace "http://www.w3.org/1999/xhtml";
}}{{Single Example
|Description=If  you declare an '''@namespace''' rule  with a prefix,  you can use the prefix  in namespace-qualified names. For example,  consider  the following namespace declaration for a namespace <code>prfx</code>.
|Code=@namespace prfx "http://prfx.contoso.com";
}}{{Single Example
|Description=Based on the previous declaration, the following selector matches <code>E</code> elements in the namespace  that  the <code>prfx</code> prefix refers to.
|Code=prfx{{!}}E
}}{{Single Example
|Description=The following code  example creates  two namespace prefixes. First, <code>p</code> elements in any namespace are colored red. Any <code>p</code> elements in the  <code>prfx</code>  namespace are then recolored blue, and <code>p</code> elements in the  <code>msft</code>  namespace are recolored green.
|Code=@namespace prfx "http://prfx.contoso.com";
@namespace msft "http://msft.example.com";
 p {background-color:red;}
prfx{{!}}p {background-color:blue;}
msft{{!}}p {background-color:green;}
}}{{Single Example
|Description=The following code  example styles a SVG element.  By using the namespace and declaration from this example, all circles  that are created with SVG  are  given a red fill.
|Code=@namespace svg "http://www.w3.org/2000/svg";
svg{{!}}circle {fill:red;}
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''@namespace''' rule  was  introduced in Windows Internet Explorer 9.
The scope of an '''@namespace''' rule is the style sheet  that  it is declared in.  You must declare an '''@namespace''' rule  after any [[css/atrules/@charset|'''@charset''']] or [[css/atrules/@import|'''@import''']] rules.
|Import_Notes====Syntax===
<code>'''@namespace '''''prfx'''''?''' ''sUrl''</code>
===Parameters===
;''prfx'':Optional. A '''String'''  value that specifies a namespace prefix.
;''sUrl'':A URL '''String'''value that specifies a namespace name.
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199783 Selectors Level 3], Section 3
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
|Topic_clusters=Syntax
|Manual_sections====Related pages (MSDN)===
*<code>Reference</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[css/cssom/styleSheet|styleSheet]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}