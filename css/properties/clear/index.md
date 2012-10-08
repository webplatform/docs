{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS Property
|Applies to=All elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=none
|Description=Default. Floating objects are allowed on both sides.
}}{{CSS Property Value
|Data Type=left
|Description=Object is moved below any floating object on the left side.
}}{{CSS Property Value
|Data Type=right
|Description=Object is moved below any floating object on the right side.
}}{{CSS Property Value
|Data Type=both
|Description=Object is moved below any floating object.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following examples use the '''clear''' attribute and the '''clear''' property to specify placement of text relative to floating objects.

This example uses a call to an embedded (global) style sheet to move the text below the floating objects when italic text is encountered.
|Code=&lt;STYLE&gt;
    I { clear:left }
&lt;/STYLE&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/clear_h.htm
}}{{Single Example
|Description=This example changes the position of the paragraph relative to the floating object on its left side.
|Code=&lt;HEAD&gt;
&lt;SCRIPT&gt;
function fnClear(){
    oClear.style.clear{{=}}"left";
}
function fnClear2(){
    oClear.style.clear{{=}}"none";
}
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
    &lt;img src{{=}}"/workshop/graphics/sphere.jpg" style{{=}}"float:left"&gt;
    &lt;SPAN ID{{=}}"oClear"&gt;
        &lt;P&gt;This is an example of the clear attribute.&lt;P&gt;
    &lt;/span&gt;
    &lt;P&gt;
        &lt;INPUT TYPE{{=}}button value{{=}}"clear {{=}} left" onclick{{=}}"fnClear()"&gt; 
        &lt;INPUT TYPE{{=}}button value{{=}}"clear {{=}} none" onclick{{=}}"fnClear2()"&gt;
    &lt;/P&gt;
&lt;/BODY&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/clear_s.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The value of this property lists the sides where floating objects are not accepted.
|Import_Notes====Syntax===
<code>'''clear: '''none '''{{!}}''' left '''{{!}}''' right '''{{!}}''' both</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.5.26
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 2.5.5
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
|Topic_clusters=Box Model
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}