{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Shorthand property that defines the [[css/properties/border-width|'''border-width''']], [[css/properties/border-style|'''border-style''']] and [[css/properties/border-color|'''border-color''']] of an element's top border in a single declaration. Note that you can use the corresponding longhand properties to set specific individual properties of the top border — [[css/properties/border-top-width|'''border-top-width''']], [[css/properties/border-top-style|'''border-top-style''']] and [[css/properties/border-top-color|'''border-top-color''']].}}
{{CSS Property
|Initial value=For style values, the initial value is none. For color values, the initial value is currentColor.  For width values, the initial value is medium, which is computed as about 3px in most browsers..
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=For <code>style</code> values, the computed value is as specified. For <code>width</code> values, the computed value is the absolute pixel value, or <code>0</code> if the value is set to <code>none</code> or <code>hidden</code>. For <code>color</code> values, the computed value is the equivalent RGB value, or the equivalent RGBA value for translucent colors.
|Animatable=No
|CSS object model property=borderTop
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=border-width border-style color
|Description=The <code>border-top</code> property can contain up to three components:
* <code>border-width</code>: This takes a numeric value with any of the standard length units.
* <code>border-style</code>: This takes any of the range of style values available to the [[css/properties/border-style|'''border-style''']] property, which includes <code>none</code>, <code>hidden</code>, <code>dotted</code>, <code>dashed</code>, <code>solid</code>, <code>double</code>, <code>groove</code>, <code>ridge</code>, <code>inset</code>, <code>outset</code>. For more details about each, see the [[css/properties/border-style|'''border-style''']] page.
* <code>color</code>: This can take any valid CSS color as its value.
}}{{CSS Property Value
|Data Type=inherit
|Description=When we set the value to <code>inherit</code>, the element will inherit the border values set on its parent.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=A simple example showing multiple <code>&lt;div&gt;</code>s, identical in style except that they have different <code>border-top</code> properties applied to them.
|Code=<div class="one"><p>One</p></div>
<div class="two"><p>Two</p></div>
<div class="three"><p>Three</p></div>
<div class="four"><p>Four</p></div>
<div class="five"><p>Five</p></div>
|LiveURL=http://code.webplatform.org/gist/5534715
}}{{Single Example
|Language=CSS
|Code=/**
 * border-top example
**/

div {
  width: 150px;
  height: 50px;
  margin: 1rem;
  float: left;
}

p {
  padding: 0.5rem;
}

.one {
  /* The most basic border-top example you can show. */ 
  border-top: 1px solid black;
}

.two {
  /* If you don't explicitly set a color, currentColor is used, which
     equates to the text colour of the element, in this case black.   */
  border-top: 4px dashed;
}

.three {
  /* When no width is specified, the default width medium is used,
     which computes to about 3px in most browsers */
  border-top: dotted red;
}

.four {
  /* When no border style is specified, the border won't appear,
     as the default border style is none. */
  border-top: 10px black;
}

.five {
  /* A more interesting border example to round things off,
     showing a basic border being set, and then the top
     border being overridden */
  border: 1px solid black;
  border-top: 10px inset rgba(234,190,50,0.75);
}
|LiveURL=http://code.webplatform.org/gist/5534715
}}
}}
{{Notes_Section
|Usage=* It is usual to use the <code>border</code> property (or properties for individual sides, e.g. <code>border-left</code>) to set the default state of a box, and then override individual values using more specific propeties, such as <code>border-width</code> or <code>border-top-color</code>.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Border
|Manual_sections====Related pages===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[css/properties/border|border]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}