{{Page_Title|margin-right}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|<code>margin-right</code> sets the right margin of an element.}}
{{CSS Property
|Initial value=Depends on the particular element. Different elements have different default margins.
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=As specified, but with relative lengths converted into absolute pixel values.
|Animatable=No
|CSS object model property=marginRight
|Values={{CSS Property Value
|Data Type=length
|Description=Specifies a fixed length, using any standard  [http://docs.webplatform.org/wiki/css/units/length CSS length units] . Negative Values are allowed.
}}{{CSS Property Value
|Data Type=percentage
|Description=A percentage of the width of the containing block. Negative values are allowed. (Even though this is margin-top, the browser will take the percentage from the width, not the height of the containing block.)
}}{{CSS Property Value
|Data Type=auto
|Description=The browser calculates a right margin dependent on the space available.
}}{{CSS Property Value
|Data Type=inherit
|Description=Inherits the parent element's specified <code>margin-right</code> width.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=In this example there are three floated blocks, styled identically except for their <code>margin-right</code> values:

* The first block has a <code>margin-right</code> of 2 centimeters, meaning that the other to blocks are pushed over to the right by 2cm. Note that a negative right margin won't make the block go outside its parent container, as is the case with a negative left margin.
* The second block has a negative right margin — -1em — which causes the third block to be pulled over to the left, overlapping the second block slightly.
* The third block has no <code>margin-right</code> of its own.
|Code=&lt;div class="one"&gt;&lt;/div&gt;
&lt;div class="two"&gt;&lt;/div&gt;
&lt;div class="three"&gt;&lt;/div&gt;
|LiveURL=http://code.webplatform.org/gist/5728056
}}{{Single Example
|Language=CSS
|Description=CSS applied to the HTML seen in the first example block.
|Code=* {
   margin: 0;
 }
 
 div {
   width: 200px;
   height: 100px;
   background: linear-gradient(rgba(0,0,0,0.25), rgba(0,0,0,0));
   border-radius: 10px;
   float: left;
 }
 
 .one {
   background-color: red;
   margin-right: 2cm;
 }
 
 .two {
   background-color: blue;
   margin-right: -1em
 }
 
 .three {
   background-color: green;
 }
|LiveURL=http://code.webplatform.org/gist/5728056
}}
}}
{{Notes_Section
|Usage====Usage===
* When calculating the height and width of an element, DO NOT include the margins in your calculations (i.e. include everything else: content area, padding, and border). However, DO include margin size when calculating available space within an element's containing element.
* When two margins collide, for example when one block level element has a right margin set, and a floated element directly to the right of it has a left margin set, the larger of the two margins remains, and the smaller one collapses and disappears.
* Margins are always transparent. 

===Best Practices===
* When possible, use [http://docs.webplatform.org/wiki/css/properties/margin margin] shorthand (i.e. {margin: 10px 15px 20px 15px;}) to specify margin-widths rather than writing out each margin's specifications as this clutters code and makes it difficult to read. Use <code>margin-bottom</code> if there is a specific reason to call attention to it (e.g. one element has a different bottom margin than the rest in its class, etc.).
|Notes====Remarks===
You can specify possible length values relative to the height of the element's font (<code>em</code>) or the height of the letter "x" (<code>ex</code>).
In Microsoft Internet Explorer 3.0, the specified margin value is added to the default value of the object. In Microsoft Internet Explorer 4.0 and later, the margin value is absolute. The margin properties do not work with the '''td''' and '''tr''' objects in Internet Explorer 4.0, but they do work in Internet Explorer 3.0. To set margins in the cell for Internet Explorer 4.0 and later, apply the margin to an object, such as '''div''' or '''p''', within the '''td'''.
This property applies to inline elements,   starting with Microsoft Internet Explorer 5.5.  With earlier versions of  Windows Internet Explorer, inline elements must have an '''absolute''' [[css/properties/position|'''position''']] or layout to use this property. Element layout is set by providing a value for the [[css/properties/height|'''height''']] property or the [[css/properties/width|'''width''']] property.
Negative margins are supported, except for top and bottom margins on inline objects.

===Standards Information===
[http://www.w3.org/TR/CSS2/box.html#propdef-margin-right w3.org]
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS 2
|URL=http://www.w3.org/TR/CSS2/box.html#propdef-margin-right
|Status=W3C Recommendation
}}
}}
{{See_Also_Section
|Topic_clusters=Box Model
|Manual_sections={{Languages}}

===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Conceptual</code>
*<code>CSS Values and Units Reference</code>
*<code>Other Resources</code>
*<code>CSS Enhancements in Internet Explorer 6</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=All
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=All
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=All
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=All
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=All
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=All
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=All
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=All
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=All
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=All
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=All
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_version=All
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=All
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}