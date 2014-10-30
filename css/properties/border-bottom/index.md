{{Page_Title|border-bottom}}
{{Flags
|State=Almost Ready
|Editorial notes=Add specifications.
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Shorthand property that defines the [[css/properties/border-width|'''border-width''']], [[css/properties/border-style|'''border-style''']] and [[css/properties/border-color|'''border-color''']] of an element's bottom border in a single declaration. Note that you can use the corresponding longhand properties to set specific individual properties of the bottom border — [[css/properties/border-bottom-width|'''border-bottom-width''']], [[css/properties/border-bottom-style|'''border-bottom-style''']] and [[css/properties/border-bottom-color|'''border-bottom-color''']].}}
{{CSS Property
|Initial value=For style values, the initial value is none. For color values, the initial value is currentColor.  For width values, the initial value is medium, which is computed as about 3px in most browsers.
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=For <code>style</code> values, the computed value is as specified. For <code>width</code> values, the computed value is the absolute pixel value, or <code>0</code> if the value is set to <code>none</code> or <code>hidden</code>. For <code>color</code> values, the computed value is the equivalent RGB value, or the equivalent RGBA value for translucent colors.
|Animatable=Yes
|CSS object model property=borderBottom
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=border-width border-style color
|Description=The <code>border-bottom</code> property can contain up to three components:
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
|Language=CSS
|Description=
|Code=/**
 * border-bottom example
**/

div {
  width: 150px;
  height: 50px;
  margin: 1rem;
  float: left;
}

p {
  padding: 0.25rem;
}

.one {
  /* The most basic border-bottom example you can show. */ 
  border-bottom: 1px solid black;
}

.two {
  /* If you don't explicitly set a color, currentColor is used, which
     equates to the text colour of the element, in this case black.   */
  border-bottom: 4px dashed;
}

.three {
  /* When no width is specified, the default width medium is used,
     which computes to about 3px in most browsers */
  border-bottom: dotted red;
}

.four {
  /* When no border style is specified, the border won't appear,
     as the default border style is none. */
  border-bottom: 10px black;
}

.five {
  /* A more interesting border example to round things off,
     showing a basic border being set, and then the bottom
     border being overridden */
  border: 1px inset black;
  border-bottom: 10px inset rgba(234,190,50,0.75);
}
|LiveURL=http://code.webplatform.org/gist/5539585
}}{{Single Example
|Language=HTML
|Description=A simple example showing multiple <code>&lt;div&gt;</code>s, identical in style except that they have different <code>border-bottom</code> properties applied to them.
|Code=&lt;div class="one"&gt;&lt;p&gt;One&lt;/p&gt;&lt;/div&gt;
&lt;div class="two"&gt;&lt;p&gt;Two&lt;/p&gt;&lt;/div&gt;
&lt;div class="three"&gt;&lt;p&gt;Three&lt;/p&gt;&lt;/div&gt;
&lt;div class="four"&gt;&lt;p&gt;Four&lt;/p&gt;&lt;/div&gt;
&lt;div class="five"&gt;&lt;p&gt;Five&lt;/p&gt;&lt;/div&gt;
|LiveURL=http://code.webplatform.org/gist/5539585
}}{{Single Example
|Language=CSS
|Description=An example showing the use of border-bottom property with the hover effect...It gives a beautiful result
|Code=/**
 * Example of border-bottom property
 
 */

#withoutBullets ul {
	color: #f06;
	font: italic 100% Georgia, serif;
	width: 500px;
	padding:10px;
	margin:10px;
	list-style-type:none;	/*To remove the default bullet style*/	
}
#withoutBullets li{
	display:inline;
	margin:8px;
	padding:4px;
}
#withoutBullets li:hover{
	border-bottom:3px solid black;
	border-radius:4px;
}
a:link{text-decoration:none;color:green;}
a:hover{text-decoration:none;color:green;}
a:active{text-decoration:none;color:green;}
a:visited{text-decoration:none;color:green;}
|LiveURL=http://code.webplatform.org/gist/5704867
}}
}}
{{Notes_Section
|Usage=* It is usual to use the <code>border-bottom</code> property to set the default state of a box's bottom border, and then override individual values using more specific propeties, such as <code>border-bottom-width</code> or <code>border-bottom-color</code>.
* <code>border-bottom</code> can be used as a divider between vertically laid out items, such as a vertical navigation menu, or table cells.
|Notes=
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
|Topic_clusters=Border
|Manual_links=
|External_links=
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/HTMLOptionElement/defaultSelected|defaultsSelected]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Reference</code>
*<code>[[css/properties/border|border]]</code>
*<code>Other Resources</code>
*<code>CSS Enhancements in Internet Explorer 6</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.0 ( 1.7 or earlier )
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=4
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=3.5
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=1.0
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=No
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=1.0 (1.0)
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_prefixed_supported=No
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}