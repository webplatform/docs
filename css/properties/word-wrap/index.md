{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS Property
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=normal
|Description=Default. Content exceeds the boundaries of its container.
}}{{CSS Property Value
|Data Type=break-word
|Description=Content wraps to next line, and a word-break occurs when necessary.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The word "blonde" is not wrappable under typical English rules.  
But, when wordWrap is set to break-word, 
the word "blonde" can be split onto two lines in any way the browser chooses: 
such as "b" and "londe", or "blo" and "nde".



The following example shows how to use the '''break-word''' value of the '''-ms-word-wrap''' property to break one long word onto multiple lines. This value avoids horizontal scrolling and can be useful for printing.  The '''p''' element in this example has layout, because its width is set.
|Code=&lt;P STYLE{{=}}"word-wrap:break-word;width:100%;left:0"&gt;
LongWordLongWord...LongWordLongWord&lt;/P&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/wordWrap.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
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
|Import_Notes====Syntax===
<code>'''-ms-word-wrap: '''normal '''{{!}}''' break-word</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203766 CSS Text Level 3], Section 7.2
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=3.5
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=5.5
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=10.5
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=1.0
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=1.0
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=1.0
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Text
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Reference</code>
*<code>[[css/properties/line-break|line-break]]</code>
*<code>[[css/properties/word-break|-ms-word-break]]</code>
*<code>[[css/properties/white-space|white-space]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}