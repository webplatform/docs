{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=Yes
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The z-index controls the stacking order of an element. Elements with a higher z-index appear closer to the viewer, whereas those with a lower z-index appear further away. Different browsers have different interpretations of the z-index ordering, so beware.}}
{{CSS Property
|Initial value=Auto
|Applies to=Positioned elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=Auto
|Description=Default. String that specifies the stacking order of the positioned objects based on the order in which the objects appear in the HTML source.
}}{{CSS Property Value
|Data Type=Integer
|Description=Integer that specifies the position of the object in the stacking order.
}}{{CSS Property Value
|Data Type=Inherit
|Description=Takes the same specified value as the property for the element's parent.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The following example demonstrates the z-index property set to auto.
|Code=.box {
  /**
   * The elements with the class `.box` are positioned absolutely
   * so as to make them overlap on each other. This helps demonstrate
   * the z-index property easily.
   */
  position: absolute;
  /**
   * The stacking order (z-index) is set to auto. Thus, the elements
   * stack in the order in which they appear in the DOM.
   */
  z-index: auto;
}

/* We offset the elements a little so the stacking order is easily seen. */
.bottom {
  top: 50px;
  left: 50px;
}

.middle {
  top: 100px;
  left: 60px;
}

.top {
  top: 150px;
  left: 70px;
}
|LiveURL=http://code.webplatform.org/gist/6199316
}}{{Single Example
|Language=HTML
|Description=The HTML for the above example.
|Code=<syntaxhighlight>
<div class="container">
    <div class="box bottom">This box is at the bottom with z-index set to auto.</div>
    <div class="box middle">This box is in the middle with z-index set to auto.</div>
    <div class="box top">This box is at the top with z-index set to auto.</div>
</div>
</syntaxhighlight>
}}{{Single Example
|Language=CSS
|Description=The following example demonstrates the z-index property set to an integer.
|Code=.box {
  /**
   * The elements with the class `.box` are positioned absolutely
   * so as to make them overlap on each other. This helps demonstrate
   * the z-index property easily.
   */
  position: absolute;
}

/* We offset the elements a little so the stacking order is easily seen. */
.bottom {
  top: 10px;
  left: 50px;
  /**
   * The stacking order position of this element is 10.
   */
  z-index: 10;
}

.middle-level-one {
  top: 60px;
  left: 60px;
  /**
   * The stacking order position of this element is greater than
   * that of `div.bottom`, thus this element will appear above `div.bottom`.
   */
  z-index: 20;
}

.middle-level-two {
  top: 120px;
  left: 70px;
  /**
   * The stacking order of this element is same as that of `div.middle-level-one`.
   * Thus, these two element will follow DOM order.
   */
  z-index: 20;
}

.top {
  top: 180px;
  left: 80px;
  /**
   * The stacking order of this element is greater than all the other elements.
   * Thus this element will appear above all of them.
   */
  z-index: 30;
}
|LiveURL=http://code.webplatform.org/gist/6199504
}}{{Single Example
|Language=HTML
|Description=The HTML for the above example.
|Code=<syntaxhighlight>
<div class="container">
    <div class="box integer top">This box is at the top with z-index set to 30.</div>
    <div class="box integer middle-level-one">This box is in the middle level 1 with z-index set to 20.</div>
    <div class="box integer middle-level-two">This box is in at middle level 2 with z-index set to 20.</div>    
    <div class="box integer bottom">This box is at the bottom with z-index set to 10.</div>
</div>
</syntaxhighlight>
}}
}}
{{Notes_Section
|Usage=This property will only work with elements that are positioned absolute, relative or fixed.
|Notes====Remarks===
If two objects have the same '''z-index''', they are stacked according to their source order. 

An element with a positive z-index will be placed above an element that does not have a defined z-index. An element with a negative z-index will be placed below an element with no defined z-index 

The property does not apply to windowed controls, such as '''select''' objects.

Only the topmost elements will receive action from a pointing device such as a mouse, even if they have a set opacity or are made invisible through CSS. This is also true for positioned elements with a negative z-index unless:
*The parent is a scrolling container (that is, its [[css/properties/overflow|'''overflow''']] property is set to '''auto''' or '''scroll''').
*The parent is positioned (that is, its [[css/properties/position|'''position''']] property is set to '''absolute''', '''relative''', or '''fixed''').
|Import_Notes====Syntax===
<code>'''z-index: '''auto '''{{!}}''' ''order''</code>
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=Negative values (CSS2.1 behavior, not allowed in CSS2 and earlier)
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=3.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=4.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=4.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
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