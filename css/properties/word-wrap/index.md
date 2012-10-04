{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_Property
|Applies to=All elements
|Media=visual
|Inherited=Yes
|Initial value=
|Values={{CSS_Property_Value|Data Type=normal |Description=Default. Content exceeds the boundaries of its container.}}
{{CSS_Property_Value|Data Type=break-word |Description=Content wraps to next line, and a word-break occurs when necessary.}}
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The word "blonde" is not wrappable under typical English rules.  
But, when wordWrap is set to break-word, 
the word "blonde" can be split onto two lines in any way the browser chooses: 
such as "b" and "londe", or "blo" and "nde".



The following example shows how to use the '''break-word''' value of the '''-ms-word-wrap''' property to break one long word onto multiple lines. This value avoids horizontal scrolling and can be useful for printing.  The '''p''' element in this example has layout, because its width is set.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/wordWrap.htm
|Code=
&lt;P STYLE{{=}}"word-wrap:break-word;width:100%;left:0"&gt;
LongWordLongWord...LongWordLongWord&lt;/P&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
Windows Internet Explorer 8. The '''-ms-word-wrap''' attribute is an extension to CSS, and can be used as a synonym for '''word-wrap''' in IE8 Standards mode.
Use this property to enable the browser to break up otherwise unbreakable strings.
This differs from the [[css/properties/white-space|'''white-space''']] 
property, which turns wrapping of the text on and off.  
The '''-ms-word-wrap''' 
property addresses only whether wrapping is permitted to occur at a place in 
the word that is not otherwise allowed by the language rules in effect.
The standards referenced below define this property's behavior as being dependent on 
the setting of the "text-wrap" property.  

However, wordWrap settings are always effective in Windows Internet Explorer 
because Internet Explorer does not support the "text-wrap" property.
This property is read-only for the '''IHTMLCurrentStyle2''' interface.
This property is read-only for the [[css/cssom/currentStyle|'''currentStyle''']] object.
This property applies to elements that have layout.  An element has layout when it is absolutely positioned, is a block element, or is an inline element with a specified height or width.
|Import_Notes=
===Syntax===
<code>'''-ms-word-wrap: '''normal '''{{!}}''' break-word</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203766 CSS Text Level 3], Section 7.2


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Reference</code>
*<code>[[css/properties/line-break|line-break]]</code>
*<code>[[css/properties/word-break|-ms-word-break]]</code>
*<code>[[css/properties/white-space|white-space]]</code>
|Topic_clusters=Text
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}