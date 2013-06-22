{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
|Editorial notes=previously imported as ms-grid-column
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Grid column provides a short hand for grid-column-start and grid-column-end. It sets an item's column positioning on a grid defined by display: grid; }}
{{CSS Property
|Initial value=1
|Applies to=grid item elements
|Inherited=No
|Computed value=Specified value
|Animatable=No
|Values={{CSS Property Value
|Data Type=integer
|Description=Integer value that identifies the specified column. 
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Syntax 
|Code=<style type="text/css">
	#mygrid { 
		display: grid; 
		grid-definition-columns: 50px; 
		grid-definition-rows: 30px;
                }
	#title { grid-column: 1/ span 4;    grid-row: 1; }
	#editor { grid-column: 1;       grid-row: 2 }
	#writer { grid-column: 2;       grid-row: 2; }
                #project{ grid-column: 3 / span 2; grid-row: 2; }
</style>

<div id="mygrid">
	<div id="A">A</div>
	<div id="B">B</div>
	<div id="C">C</div>
</div>
}}
}}
{{Notes_Section
|Notes====Remarks===
The column numbering system is a 1-based index, with 1 being the default. That is, column numbering does not begin with zero.
|Import_Notes====Syntax===
<code>'''-ms-grid-column: '''''
&lt;integer&gt;
''</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}215213 CSS Grid Layout], Section 6
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
|Topic_clusters=Grid Layout
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[html/elements/a|a]]</code>
*<code>abbr</code>
*<code>[[html/elements/acronym|acronym]]</code>
*<code>b</code>
*<code>bdo</code>
*<code>big</code>
*<code>br</code>
*<code>cite</code>
*<code>code</code>
*<code>dfn</code>
*<code>em</code>
*<code>i</code>
*<code>img</code>
*<code>input</code>
*<code>kbd</code>
*<code>label</code>
*<code>q</code>
*<code>samp</code>
*<code>select</code>
*<code>small</code>
*<code>span</code>
*<code>strong</code>
*<code>sub</code>
*<code>sup</code>
*<code>textArea</code>
*<code>tt</code>
*<code>var</code>
*<code>address</code>
*<code>blockQuote</code>
*<code>div</code>
*<code>dl</code>
*<code>fieldSet</code>
*<code>form</code>
*<code>noFrames</code>
*<code>noScript</code>
*<code>ol</code>
*<code>p</code>
*<code>pre</code>
*<code>[[html/elements/table|table]]</code>
*<code>ul</code>
*<code>dd</code>
*<code>dt</code>
*<code>li</code>
*<code>tBody</code>
*<code>td</code>
*<code>tFoot</code>
*<code>th</code>
*<code>tHead</code>
*<code>tr</code>
*<code>button</code>
*<code>del</code>
*<code>ins</code>
*<code>map</code>
*<code>object</code>
*<code>script</code>
*<code>[[css/properties/ms-grid-columns|-ms-grid-columns]]</code>
*<code>[[css/properties/ms-grid-row|-ms-grid-row]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}