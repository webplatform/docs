{{Page_Title}}
{{Flags
|Content=Compatibility Incomplete, Examples Best Practices
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The '''clear''' CSS property specifies if an element can be positioned next to or must be positioned below the [[css/properties/float|floating]] elements that precede it in the markup.}}
{{CSS Property
|Initial value=none
|Applies to=Block-level elements
|Inherited=No
|Media=visual
|Computed value=as specified
|Animatable=No
|CSS object model property=clear
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=none
|Description=May have adjacent floats on both the left and right sides.
}}{{CSS Property Value
|Data Type=left
|Description=Floated elements that precede the cleared element are not allowed to the left of the cleared element. The cleared element must move below the floated element.
}}{{CSS Property Value
|Data Type=right
|Description=Floated elements that precede the cleared element are not allowed to the right of the cleared element. The cleared element must move below the floated element.
}}{{CSS Property Value
|Data Type=both
|Description=Floated elements that precede the cleared element are not allowed to be adjacent to the cleared element. The cleared element must move below the floated elements.
}}{{CSS Property Value
|Data Type=inherit
|Description=Takes the same specified value as the property for the element's parent.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Check the live example to see how these classes are applied to headlines.
|Code=.left {
	border: 1px solid black;
	clear: left;
}
.both {
	border: 1px solid black;
	clear: both;
}
|LiveURL=https://developer.mozilla.org/samples/cssref/clear.html
}}{{Single Example
|Language=HTML
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
|Notes=<div class='license-cc-by-sa'>The '''clear''' property applies to both [[css/properties/float|floating]] and non-floating elements.

When applied to non-floating blocks, it moves the [[css/properties/border|border]] edge of the element down until it is below the margin edge of all relevant floats. This movement (when it happens) causes margin collapsing not to occur.

When applied to floating elements, it moves the margin edge of the element below the margin edge of all relevant floats. This affects the position of later floats, since later floats cannot be positioned higher than earlier ones.

The floats that are relevant to be cleared are the earlier floats within the same block formatting context.</div>
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
|Manual_links=* [[tutorials/floats_and_clearing|Tutorial: Page layout with floats and clearing]].
* [[tutorials/box_model|Tutorial: Exploring the CSS box model]].
* [[guides/the_css_layout_model|Guide: The CSS layout model]].
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
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/clear
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}