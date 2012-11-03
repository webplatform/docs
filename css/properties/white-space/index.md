{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The white-space property controls if a white-space character within an element can wrap or if it must be preserved.}}
{{CSS Property
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=normal
|Description=Default. Lines of text break automatically. Content wraps to the next line if it exceeds the width of the object.
}}{{CSS Property Value
|Data Type=nowrap
|Description=Line breaks are suppressed. Content does not wrap to the next line.
}}{{CSS Property Value
|Data Type=pre
|Description=Line breaks and other whitespace are preserved. This possible value is supported starting in Internet Explorer 6 when the [[html/elements/!DOCTYPE|!DOCTYPE]] declaration specifies standards-compliant mode. When the !DOCTYPE declaration does not specify standards-compliant mode, you can retrieve this value, but it does not affect rendering—it functions like the '''normal''' value.
}}{{CSS Property Value
|Data Type=pre-line
|Description=Sequences of line breaks are preserved.
}}{{CSS Property Value
|Data Type=pre-wrap
|Description=Sequences of line breaks are collapsed.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example shows how automatic line breaks are suppressed when the user places the mouse pointer over the paragraph. This is caused by toggling the value of the '''white-space''' attribute in the [[dom/events/mouseover|'''onmouseover''']] and [[dom/events/mouseout|'''onmouseout''']] events of the '''p''' element. When the '''white-space''' attribute is set to '''nowrap''' in the '''onmouseover''' event, line breaks are suppressed, and horizontal scrolling is required to view content wider than the element.  When the attribute is set to '''normal''' in the '''onmouseout''' event, lines break automatically, depending on the width of the element.
|Code=&lt;html&gt;
&lt;head&gt;
&lt;style type{{=}}"text/css"&gt;
.clsOneLiner {
    white-space: nowrap;
}
.clsAutoBreak {
    white-space: normal;
}
&lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;p onmouseover{{=}}"this.className{{=}}'clsOneLiner';" 
    onmouseout{{=}}"this.className{{=}}'clsAutoBreak';"&gt;
Long lines of text remain unbroken when the value of the whitespace attribute is 
set to nowrap. Place your mouse over the text to suppress automatic line breaks.&lt;/p&gt;
&lt;/body&gt;
&lt;/html&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/whitespace.htm
}}{{Single Example
|Description=The following example shows how to set and retrieve the value of the '''white-space''' property. When the user sets the value of the '''white-space''' property of a '''div''' element, the value of the property is retrieved in a '''span''' element.
|Code=&lt;!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN"&gt;
&lt;html&gt;
&lt;head&gt;
&lt;script type{{=}}"text/javascript"&gt;
function fnSwitch(){
  oDiv.style.whiteSpace {{=}} event.srcElement.innerText;
  document.all.oSpan.innerText {{=}} oDiv.currentStyle.whiteSpace;
}
&lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;h1&gt;direction Property Sample&lt;/h1&gt;
&lt;h2&gt;direction: 
&lt;span id{{=}}"oSpan" style{{=}}"color: red"&gt;&lt;/span&gt;&lt;/h2&gt;
&lt;p&gt;[ &lt;a href{{=}}"#" onclick{{=}}"fnSwitch()"&gt;normal&lt;/a&gt; {{!}} 
&lt;a href{{=}}"#" onclick{{=}}"fnSwitch()"&gt;nowrap&lt;/a&gt; {{!}} 
&lt;a href{{=}}"#" onclick{{=}}"fnSwitch()"&gt;pre&lt;/a&gt; 
]&lt;/p&gt;
&lt;div id{{=}}"oDiv" style{{=}}"background: #e4e4e4; padding: 10px;"&gt;
    In   the   source,   this   sentence   has   three   spaces   between   each   word. 
    This sentence 
    takes up three lines 
    in the source. &lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/whitespace_1.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
Whitespace, such as line breaks, spaces, and tabs, is collapsed by default in HTML documents. You can use the nonbreaking space entity <code>(&amp;nbsp;)</code> to add extra spaces to an object when the '''white-space''' property is set to '''normal''' or '''nowrap'''.  You can add extra line breaks using the '''br''' element.
This property affects content you access through the Document Object Model (DOM) the same way it affects the way Windows Internet Explorer displays the content.
Still in Internet Explorer 6, this property applies to the [[css/cssom/currentStyle|'''currentStyle''']] element. The '''pre''' value of this property is now supported.
Windows Internet Explorer 8. The '''pre-line''' and '''pre-wrap''' values are used to control sequences of whitespace. A value of '''pre-line''' instructs Windows Internet Explorer to combine multiple line breaks into a single line, whereas '''pre-wrap''' wraps each newline onto a separate line. Inside a '''pre''' block, lines breaks occur at newlines in the source, at occurrences of "\A" in generated content ([[css/selectors/pseudo-elements/::before|'''::before''']] and [[css/selectors/pseudo-elements/::after|'''::after''']]), and as necessary to fill line boxes.
|Import_Notes====Syntax===
<code>'''white-space: '''normal '''{{!}}''' pre '''{{!}}''' nowrap '''{{!}}''' pre-wrap '''{{!}}''' pre-line</code>
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Text
|Manual_sections====Related pages (MSDN)===
*<code>[[css/selectors/pseudo-elements/::after|:after]]</code>
*<code>[[css/selectors/pseudo-elements/::before|:before]]</code>
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Reference</code>
*<code>pre</code>
*<code>[[css/properties/word-wrap|-ms-word-wrap]]</code>
*<code>Other Resources</code>
*<code>CSS Enhancements in Internet Explorer 6</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}