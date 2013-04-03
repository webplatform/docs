{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|This property indicates which sides of an element's box(es) may not be adjacent to an earlier floating box. The '''clear''' property does not consider floats inside the element itself or in other block formatting contexts.}}
{{CSS Property
|Initial value=none
|Applies to=Block-level elements
|Inherited=No
|Media=visual
|Computed value=as specified
|Animatable=No
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=none
|Description=No constraint on the box's position with respect to floats.
}}{{CSS Property Value
|Data Type=left
|Description=Requires that the top border edge of the box be below the bottom outer edge of any left-floating boxes that resulted from elements earlier in the source document.
}}{{CSS Property Value
|Data Type=right
|Description=Requires that the top border edge of the box be below the bottom outer edge of any right-floating boxes that resulted from elements earlier in the source document.
}}{{CSS Property Value
|Data Type=both
|Description=Requires that the top border edge of the box be below the bottom outer edge of any right-floating and left-floating boxes that resulted from elements earlier in the source document.
}}{{CSS Property Value
|Data Type=inherit
|Description=Takes the same specified value as the property for the element's parent.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following examples use the '''clear''' attribute and the '''clear''' property to specify placement of text relative to floating objects.

This example uses a call to an embedded (global) style sheet to move the text below the floating objects when italic text is encountered.
|Code=&lt;style&gt;
    i { clear:left }
&lt;/style&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/clear_h.htm
}}{{Single Example
|Description=This example changes the position of the paragraph relative to the floating object on its left side.
|Code=&lt;script&gt;
function fnClear(){
    oClear.style.clear{{=}}"left";
}
function fnClear2(){
    oClear.style.clear{{=}}"none";
}
&lt;/script&gt;
    &lt;img src{{=}}"/workshop/graphics/sphere.jpg" style{{=}}"float:left"&gt;
    &lt;span id{{=}}"oClear"&gt;
        &lt;p&gt;This is an example of the clear attribute.&lt;p&gt;
    &lt;/span&gt;
    &lt;p&gt;
        &lt;input type{{=}}"button" value{{=}}"clear {{=}} left" onclick{{=}}"fnClear()"&gt; 
        &lt;input type{{=}}"button" value{{=}}"clear {{=}} none" onclick{{=}}"fnClear2()"&gt;
    &lt;/p&gt;
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
|Specifications={{Related Specification
|Name=Cascading Style Sheets Level 2 Revision 1 (CSS 2.1) Specification
|URL=http://www.w3.org/TR/CSS2/visuren.html#propdef-clear
|Status=Recomendation
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