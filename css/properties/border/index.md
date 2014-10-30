{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Add specification details and links.
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Shorthand property that defines the different properties of all four sides of an element's border in a single declaration. It can be used to set [[css/properties/border-width|border-width]], [[css/properties/border-style|border-style]] and [[css/properties/border-color|border-color]], or a subset of these.}}
{{CSS Property
|Initial value=medium none currentColor
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=concatenation of <code>border-width</code>, <code>border-style</code>, and <code>border-color</code>.
|Animatable=Yes
|CSS object model property=border
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=inherit
|Description=When the value is set to <code>inherit</code>, the element will inherit the border values set on its parent.
}}{{CSS Property Value
|Data Type=<border-width> OR <border-style> OR <border-color>
|Description=A concatenation of <code>&lt;border-width&gt;</code>, <code>&lt;border-style&gt;</code>, and <code>&lt;border-color&gt;</code>. At least one of these must be present, and they may appear in any order.

'''<border-width>''': A numeric value with any of the standard length units. The initial value is <code>medium</code>, which most browsers will render as 3px. See the [[css/properties/border-width|border-width]] property.

'''<border-style>''': This takes any of the range of values available to the [[css/properties/border-style|border-style]] property. The initial value is <code>none</code>.

'''<border-color>''': This takes any valid CSS color. See the [[css/properties/border-color|border-color]] property. The initial value is <code>currentColor</code>.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=A simple example showing multiple <code>&lt;div&gt;</code>s, identical in style except that they have different <code>border</code> properties applied to them.
|Code=&lt;div class="one"&gt;&lt;p&gt;One&lt;/p&gt;&lt;/div&gt;
&lt;div class="two"&gt;&lt;p&gt;Two&lt;/p&gt;&lt;/div&gt;
&lt;div class="three"&gt;&lt;p&gt;Three&lt;/p&gt;&lt;/div&gt;
&lt;div class="four"&gt;&lt;p&gt;Four&lt;/p&gt;&lt;/div&gt;
&lt;div class="five"&gt;&lt;p&gt;Five&lt;/p&gt;&lt;/div&gt;
|LiveURL=http://code.webplatform.org/gist/5534182
}}{{Single Example
|Language=CSS
|Description=
|Code=/**
 * border example
**/

div {
  width: 150px;
  height: 150px;
  margin: 1rem;
  float: left;
}

p {
  padding: 2rem;
}

.one {
  /* The most basic border example you can show. */ 
  border: 1px solid black;
}

.two {
  /* If you don't explicitly set a color, currentColor is used, which
     equates to the text colour of the element, in this case black.   */
  border: 4px dashed;
}

.three {
  /* When no width is specified, the default width medium is used,
     which computes to about 3px in most browsers */
  border: dotted red;
}

.four {
  /* When no border style is specified, the border won't appear,
     as the default border style is none. */
  border: 10px black;
}

.five {
  /* A more interesting border example to round things off. */
  border: 10px inset rgba(234,190,50,0.75);
}
|LiveURL=http://code.webplatform.org/gist/5534182
}}
}}
{{Notes_Section
|Usage=* It is usual to first use the <code>border</code> shorthand property to set the state of a default box, and then override it where needed, using the more specific shorthand properties <code>[[css/properties/border-width|border-width]]</code>, <code>[[css/properties/border-style|border-style]]</code>, and <code>[[css/properties/border-color|border-color]]</code>. Each of these properties may take up to four values, respective to the sides of the box.
* It is also common to override the <code>border</code> property with the properties specific to each individual side: <code>[[css/properties/border-top|border-top]]</code>, <code>[[css/properties/border-right|border-right]]</code>, <code>[[css/properties/border-bottom|border-bottom]]</code>, and <code>[[css/properties/border-left|border-left]]</code>. Each of these properties may take up to three values, defining the appearance (width, style, and color) of the designated side.
* The following twelve "longhand" properties can be used to define the entire border of an object:
<code>[[css/properties/border-top-width|border-top-width]]</code>,
<code>[[css/properties/border-top-style|border-top-style]]</code>,
<code>[[css/properties/border-top-color|border-top-color]]</code>,
<code>[[css/properties/border-right-width|border-right-width]]</code>,
<code>[[css/properties/border-right-style|border-right-style]]</code>,
<code>[[css/properties/border-right-color|border-right-color]]</code>,
<code>[[css/properties/border-bottom-width|border-bottom-width]]</code>,
<code>[[css/properties/border-bottom-style|border-bottom-style]]</code>,
<code>[[css/properties/border-bottom-color|border-bottom-color]]</code>,
<code>[[css/properties/border-left-width|border-left-width]]</code>,
<code>[[css/properties/border-left-style|border-left-style]]</code>,
<code>[[css/properties/border-left-color|border-left-color]]</code>.
|Notes=* The initial value of <code>border</code> is the concatenated result of the initial values of each component.
* A <code>border-bottom</code> can be used as a divider between vertically laid out items, such as navigation menu items, or a new section. Authors will sometimes use this technique rather than inserting an <code>[[html/elements/hr|&lt;hr/&gt;]]</code> element in the HTML.
* Another common technique is to use <code>border-bottom</code> properties for link underlining rather than <code>text-decoration: underline</code>, as it affords the designer more control.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Level 3
|URL=http://www.w3.org/TR/css3-background/#borders
|Status=Candidate Recommendation
|Relevant_changes=
}}{{Related Specification
|Name=CSS Level 2 (Revision 1)
|URL=http://www.w3.org/TR/CSS2/box.html#border-shorthand-properties
|Status=Recommendation
|Relevant_changes=
}}{{Related Specification
|Name=CSS Level 1
|URL=http://www.w3.org/TR/CSS1/#border
|Status=Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Topic_clusters=Border, Box Model
|Manual_links=
|External_links=
|Manual_sections====Related pages===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/HTMLOptionElement/defaultSelected|defaultSelected]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}