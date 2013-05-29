{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS Property
|Initial value=normal
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Computed value=normal or absolute length
|Animatable=No
|CSS object model property=letterSpacing
|Values={{CSS Property Value
|Data Type=normal
|Description=The spacing is the normal spacing for the current font.
}}{{CSS Property Value
|Data Type=length
|Description=Indicates inter-character space in addition to the default space between characters, followed by an absolute units designator (cm, mm, in, pt, or pc) or a relative units designator (em, ex, or px). Values may be negative, but there may be implementation-specific limits.
}}
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example shows how to use the '''word-spacing''' attribute and the '''word-spacing''' property to increase the amount of space between words in a '''span'''.
|LiveURL=
|Code=
&lt;STYLE&gt;
   SPAN.spacing{word-spacing: 10;}
&lt;/STYLE&gt;
&lt;SCRIPT&gt;
function fnChangeSpace(){
    oSpan.style.wordSpacing {{=}} 
       oSelSpace.options[oSelSpace.selectedIndex].text;
}
&lt;/SCRIPT&gt;
&lt;SELECT ID {{=}} "oSelSpace" onchange {{=}} "fnChangeSpace()"&gt;
   &lt;OPTION&gt;10
   &lt;OPTION&gt;15
   &lt;OPTION&gt;20
&lt;/SELECT&gt;
&lt;SPAN ID {{=}} "oSpan" CLASS {{=}} "spacing"&gt;
The quick brown fox jumped over the lazy dog.
&lt;/SPAN&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''word-spacing''' property is 
available on Macintosh beginning with Microsoft Internet Explorer 4.01. It is available for other platforms beginning with Microsoft Internet Explorer 6.
This attribute adds the specified spacing after each word. Justification can influence word spacing.
The length value indicates an addition to the default space between words. Negative values are permitted.
In Internet Explorer 6, This property now applies to the [[css/cssom/currentStyle|'''currentStyle''']] element.
|Import_Notes=
===Syntax===
<code>'''word-spacing: '''normal '''{{!}}''' ''
&lt;length&gt;
''</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.4.1


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>CSS Enhancements in Internet Explorer 6</code>
|Topic_clusters=Text
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}