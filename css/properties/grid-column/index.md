{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Content=Compatibility Incomplete, Examples Needed
|Checked_Out=No
|Editorial notes=Previously imported as ms-grid-column.
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Shorthand for setting [[css/properties/grid-column-start|grid-column-start]] and [[css/properties/grid-column-end|grid-column-end]] in a single declaration.}}
{{CSS Property
|Initial value=See individual properties
|Applies to=Grid items
|Inherited=No
|Media=visual
|Computed value=See individual properties
|Animatable=No
|CSS percentages=See individual properties
|Values={{CSS Property Value
|Data Type=<grid-line> [ / <grid-line> ]
|Description=If two <grid-line> values are specified, the grid-column-start property is set to the value before the slash, and the grid-column-end property is set to the value after the slash. If the second value is omitted, then if the first value is an identifier (<ident>), the grid-column-end property is also set to that <ident>; otherwise, it is set to "auto".
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=<pre>
<!DOCTYPE html>
<html >
<head>
    <title>Simple grid example</title>
  <style type="text/css">
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

&lt;/head&gt;
&lt;body&gt;
&lt;div id="mygrid"&gt;
	&lt;div id="title"&gt;&lt;h1&gt;"Writer - editor   
 projects"&lt;/h1&gt;&lt;/div&gt;
	&lt;div id="editor"&gt;John Sterling</div&gt;
	&lt;div id="writer"&gt;Chuck Brown</div&gt;
                 &lt;div id="project"&gt;Webplatform.org CSS property descriptions.&lt;/div&gt;
&lt;/div&gt;

&lt;/body&gt;
&lt;/html&gt;
</pre>
|LiveURL=http://code.webplatform.org/gist/5842103
}}{{Single Example
|Language=CSS
|Code=<pre>
<!DOCTYPE html>
<html >
<head>
    <title>Simple grid example</title>
  <style type="text/css">
	#mygrid { 
		display: grid; 
		grid-definition-columns: 
                                        "title" auto
                                        "editors"  200px 
                                        "writers"  200px
                                        "projects" 400px
                                         ;
		grid-definition-rows: 30px;
	}
	#title { grid-column: "titles"/ span 4;    grid-row: 1; }
	#editor { grid-column: "editors";       grid-row: 2 }
	#writer { grid-column: "writers";       grid-row: 2; }
                #project{ grid-column: "projects" / span 2; grid-row: 2; }
</style>

&lt;/head&gt;
&lt;body&gt;
&lt;div id="mygrid"&gt;
	&lt;div id="title"&gt;&lt;h1&gt;"Writer - editor   
 projects"&lt;/h1&gt;&lt;/div&gt;
	&lt;div id="editor"&gt;John Sterling</div&gt;
	&lt;div id="writer"&gt;Chuck Brown</div&gt;
                 &lt;div id="project"&gt;Webplatform.org CSS property descriptions.&lt;/div&gt;
&lt;/div&gt;

&lt;/body&gt;
&lt;/html&gt;
</pre>
|LiveURL=http://code.webplatform.org/gist/5842400
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C Grid Layout Module
|URL=http://www.w3.org/TR/css3-grid-layout
|Status=W3C Working Draft
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