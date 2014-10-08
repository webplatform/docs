{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The <code>box-sizing</code> property alters the CSS box model used to calculate widths and heights of elements, so that they can be equal to the width and height of the content-, padding- or border-box.}}
{{CSS Property
|Initial value=content-box
|Applies to=all elements that accept width or height
|Inherited=No
|Media=visual
|Computed value=specified value
|Animatable=Yes
|CSS object model property=
|CSS percentages=
|Values={{CSS Property Value
|Data Type=content-box
|Description=The <code>width</code> and <code>height</code> properties (also including <code>min-width</code>, <code>max-width</code>, <code>min-height</code> and <code>max-height</code> properties) are calculated as the width/height of the content, but not the border, margin, or padding. This is the traditional behaviour of width and height as specified by CSS2.1.
}}{{CSS Property Value
|Data Type=padding-box
|Description=The <code>width</code> and <code>height</code> (also including <code>min-width</code>, <code>max-width</code>, <code>min-height</code> and <code>max-height</code> properties) of an element are calculated as the width/height of the content plus the <code>padding</code>. The dimensions of the content alone are thus calculated by subtracting the padding widths from each side of the element. Dimension properties are set to 0 if the calculated value is less than 0.
}}{{CSS Property Value
|Data Type=border-box
|Description=The <code>width</code> and <code>height</code> (also including <code>min-width</code>, <code>max-width</code>, <code>min-height</code> and <code>max-height</code> properties) of an element are calculated as the width/height of the content plus the <code>padding</code> and <code>border</code>.
The dimensions of the content alone are thus calculated by subtracting the padding and border widths from each side of the element. Dimension properties are set to 0 if the calculated value is less than 0.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following examples assume markup that looks like this.
|Code=&lt;div class="parent"&gt;
	&lt;div class="child"&gt;&lt;/div&gt;
&lt;/div&gt;
|LiveURL=
}}{{Single Example
|Language=CSS
|Description=This CSS makes it so that the child <code>&lt;div&gt;</code> will always An element with padding that occupies half the width of its parent. This works because it has <code>box-sizing: border-box</code> set on it, so the total width will always be content plus padding plus border. As the border and padding get thicker, the element doesn't get larger. Instead, the content gets smaller to make way for the change.
|Code=/* Support Firefox, WebKit, Opera and IE8+ */

.parent {
   width: 50%;
   height: 200px;
   background: red;
 }
 
 .child {   
	border: 30px solid rgba(0,0,0,0.5); 
	float: left;
	padding: 3rem;
	background: blue;
	width: 50%;
	height: 100px;
	box-sizing: border-box;
 }
|LiveURL=http://code.webplatform.org/gist/5496267
}}{{Single Example
|Language=CSS
|Description=Input elements with type <code>search</code> are rendered with <code>border-box</code> in Safari 5 and Chrome. You can normalize this behavior across all browsers using the following code.
|Code=input[type="search"] {
	box-sizing: content-box;
}
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Level 3 - Basic User Interface Module
|URL=http://www.w3.org/TR/css3-ui/#box-sizing
|Status=W3C Working Draft
|Relevant_changes=
}}
}}
{{See_Also_Section
|Topic_clusters=Box Model
|Manual_links=* [http://docs.webplatform.org/wiki/tutorials/box_model WebPlatform.org tutorial on Box Model]
|External_links=* A [http://css-tricks.com/box-sizing/ detailed article on box-sizing] by Chris Coyier.
* Paul Irish wrote about [http://paulirish.com/2012/box-sizing-border-box-ftw/ applying <code>box-sizing: border-box;</code> on all elements].
|Manual_sections=
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/box-sizing
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809 Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=Basic Support
|Chrome_supported=Yes
|Chrome_version=9
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=1
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=Yes
|Firefox_prefixed_version=1
|Internet_explorer_supported=Yes
|Internet_explorer_version=8
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=9.5
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.1
|Safari_prefixed_supported=Yes
|Safari_prefixed_version=3.1
}}{{Compatibility Table Desktop Row
|Feature=padding-box
|Chrome_supported=No
|Chrome_version=
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=Yes
|Firefox_prefixed_version=1
|Internet_explorer_supported=No
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=4.0
|Android_prefixed_supported=Yes
|Android_prefixed_version=2.1
|Blackberry_supported=Yes
|Blackberry_version=10
|Blackberry_prefixed_supported=Yes
|Blackberry_prefixed_version=7
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=18
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=29
|Firefox_mobile_prefixed_supported=Yes
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=10
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_version=5.0
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=5.0
|Safari_mobile_prefixed_supported=Yes
|Safari_mobile_prefixed_version=3.2
}}{{Compatibility Table Mobile Row
|Feature=padding-box
|Android_supported=No
|Android_version=
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=No
|Blackberry_version=
|Blackberry_prefixed_supported=No
|Blackberry_prefixed_version=
|Chrome_mobile_supported=No
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=29
|Firefox_mobile_prefixed_supported=Yes
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}