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
|Values={{CSS_Property_Value|Data Type=left |Description=Default. Text is aligned to the left.}}
{{CSS_Property_Value|Data Type=right |Description=Text is aligned to the right.}}
{{CSS_Property_Value|Data Type=center |Description=Text is centered.}}
{{CSS_Property_Value|Data Type=justify |Description=Text is justified.}}
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following examples use the '''text-align''' attribute and the '''text-align''' property to align text within the object.

This example uses '''p''' as a selector and two classes to call an embedded style sheet that aligns the text according to the respective rule.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/text-align.htm
|Code=
&lt;STYLE&gt;
    P { text-align:center }
    .align1 { text-align:right }
    .align2 { text-align:justify }
&lt;/STYLE&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;P onclick{{=}} "this.className{{=}}'align1'" 
    ondblclick{{=}}"this.className{{=}}'align2'"&gt;
. . . &lt;/P&gt;
}}
{{Single_Example
|Description=This example uses inline scripting to change the alignment of the text when an [[dom/events/mouseover|'''onmouseover''']] event occurs.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/textAlign.htm
|Code=
&lt;P STYLE{{=}}"font-size:14" 
    onmouseover{{=}}"this.style.textAlign{{=}}'center'"&gt;
. . . &lt;/P&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The property applies to block elements. The property is inherited by all block-level objects inside a '''div''' object. This parameter receives null if the attribute is not set.
The '''justify''' possible value is available as of Microsoft Internet Explorer 4.0.
|Import_Notes=
===Syntax===
<code>'''text-align: '''left '''{{!}}''' right '''{{!}}''' center '''{{!}}''' justify</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.4.6


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
|Topic_clusters=Text
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}