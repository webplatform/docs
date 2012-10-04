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
|Values={{CSS_Property_Value|Data Type=none |Description=Default. Text is not transformed.}}
{{CSS_Property_Value|Data Type=capitalize |Description=Transforms the first character of each word to uppercase.}}
{{CSS_Property_Value|Data Type=uppercase |Description=Transforms all the characters to uppercase.}}
{{CSS_Property_Value|Data Type=lowercase |Description=Transforms all the characters to lowercase.}}
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following examples use the '''text-transform''' attribute and the '''text-transform''' property to transform a block of text from lower case to upper case when the user moves the mouse over the text. The text transforms back to lower case when the user clicks the text.

This example uses three calls to an embedded (global) style sheet to transform the text.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/text-transform.htm
|Code=
&lt;STYLE&gt;
    .transform1 { text-transform:uppercase }
    .transform2 { text-transform:lowercase }
    .transform3 { text-transform:none }
&lt;/STYLE&gt;
&lt;/HEAD&gt;
&lt;BODY&gt; 
&lt;DIV STYLE{{=}}"font-size:14" 
    onmouseover{{=}}"this.className{{=}}'transform1'" 
    onclick{{=}} "this.className{{=}}'transform2'"
    ondblclick{{=}}"this.className{{=}}'transform3'"&gt; 
:
&lt;/DIV&gt;
}}
{{Single_Example
|Description=This example uses inline scripting to transform the text when different mouse events occur.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/textTransform.htm
|Code=
&lt;DIV STYLE{{=}}"font-size:14"
    onmouseover{{=}}"this.style.textTransform{{=}}'uppercase'"
    onmouseout{{=}}"this.style.textTransform{{=}}'lowercase'"
    onclick{{=}}"this.style.textTransform{{=}}'none'"&gt;
:
&lt;/DIV&gt;
}}}}
{{Notes_Section
|Import_Notes=
===Syntax===
<code>'''text-transform: '''capitalize '''{{!}}''' uppercase '''{{!}}''' lowercase '''{{!}}''' none</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.4.5


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
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