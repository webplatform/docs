{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=<length/percentage> hanging and <length/percentage> each-line currently an experimental feature in CSS Text Level 3 or just experimental, unclear
|Checked_Out=No
|Content=Incomplete
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Specifies the amount of space horizontally that should be left on the first line of the text of an element. This horizontal spacing is at the beginning of the first line and is in respect to the left edge of the containing block box.}}
{{CSS Property
|Initial value=0
|Applies to=Block, inline-block, and table cells
|Inherited=Yes
|Media=visual
|Computed value=percentage or absolute length
|Animatable=No
|CSS object model property=textIndent
|CSS percentages=refer to width of containing block
|Values={{CSS Property Value
|Data Type=length
|Description=Floating-point number, followed by an absolute units designator (cm, mm, in, pt, or pc) or a relative units designator (em, ex, or px).
}}{{CSS Property Value
|Data Type=percentage
|Description=Integer, followed by a percent sign (%). This value is a percentage of the width of the parent object.
}}{{CSS Property Value
|Data Type=inherit
|Description=Inherits the value from the cascade.
}}{{CSS Property Value
|Data Type=&lt;length/percentage&gt; each-line
|Description=This value can only be used in conjunction with a length or percentage value (<code>text-indent: 7px each-line;</code>). It will affect not only the first line of the block container but also any line that is after a forced line break. This does not have affect on soft wrap break.

Currently experimental in CSS Text Level 3
}}{{CSS Property Value
|Data Type=&lt;length/percentage&gt; hanging
|Description=This value can only be used in conjunction with a length or percentage value (<code>text-indent: 7px hanging;</code>). It inverts which lines are indented so that everything but the first formatted line is indented. 

Currently an experimental feature.
}}{{CSS Property Value
|Data Type=&lt;length/percentage&gt; each-line
|Description=This value can only be used in conjunction with a length or percentage value (<code>text-indent: 7px each-line;</code>). It indents all lines in the element, not just the first line.

Currently an experimental feature.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The following examples use the '''text-indent''' attribute and the '''text-indent''' property to indent the object's text.

This example uses calls to an embedded style sheet to change the indent on the text when a [[dom/events/click|'''click''']] event occurs. The text was originally indented 2 centimeters using '''div''' as a selector in the style sheet.
|Code=/* Indenting a line by an absolute value. */
p:nth-child(1) {
	text-indent: 3em;
}

/* Indenting a line by an absolute value, but with the `hanging` keyword. */
p:nth-child(2) {
	text-indent: 3em hanging;
}

/* Indenting a line by a percentage (the width used is the distance from the beginning to the end of the line.) */
p:nth-child(3) {
	text-indent: 50%;
}
|LiveURL=http://code.webplatform.org/gist/5842068
}}{{Single Example
|Language=HTML
|Description=This example uses JavaScript to indent the text within the '''div''' when a [[dom/events/mouseover|'''mouseover''']] event occurs.
|Code=&lt;!DOCTYPE html&gt;
&lt;html&gt;
 &lt;head&gt;
 &lt;title&gt;Example&lt;/title&gt;
  &lt;script&gt;
function initialize() {
  var element = document.getElementById("example");
  element.addEventListener("mouseover", function () {
    this.style.textIndent = "2cm";
  }, false);
}
window.addEventListener("load", initialize, false);
  &lt;/script&gt;
 &lt;/head&gt;
 &lt;body&gt;
  &lt;div id="example"&gt;Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin condimentum malesuada quam, ut ullamcorper nunc posuere in. Duis ullamcorper fringilla lorem eget accumsan. Praesent neque ipsum, tincidunt eget aliquet sit amet, tempor eget felis. Duis nibh magna, vestibulum et molestie sed, porttitor vel tellus. Nunc suscipit justo ut magna imperdiet pharetra. Suspendisse potenti. Vivamus vestibulum, dui eu fermentum blandit, nunc dolor aliquet massa, non elementum arcu arcu ut risus. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Suspendisse tincidunt nibh at ipsum semper eu tempor nisi ornare. Nunc vestibulum elementum dapibus. Morbi pellentesque nulla non est adipiscing id commodo eros blandit. Suspendisse mauris tellus, auctor a sodales a, consequat nec diam.&lt;/div&gt;
 &lt;/body&gt;
&lt;/html&gt;
|LiveURL=http://code.webplatform.org/gist/5658652
}}
}}
{{Notes_Section
|Usage=It is important to note that the keyword options ('''each-line''' and '''hanging''') are experimental features; exercise caution when using them, as there is no guarantee of cross-browser compatibility.
|Notes=The property can be negative. An indent is not inserted in the middle of an object that was broken by another object, such as '''br''' in HTML.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Text Module Level 3
|URL=http://www.w3.org/TR/css3-text/
|Status=Working Draft
|Relevant_changes=Section 9.1. (Adds hanging and each-line as supplemental keywords)
}}{{Related Specification
|Name=CSS 2.1
|URL=http://www.w3.org/TR/CSS2/
|Status=Recommendation
|Relevant_changes=Section 5.4.7
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=3.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=3.5
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=<em>hanging</em> keyword
|Chrome_supported=No
|Chrome_version=
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
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
|Safari_prefixed_supported=Yes
|Safari_prefixed_version=7 (unofficial yet)
}}{{Compatibility Table Desktop Row
|Feature=<em>each-line</em> keyword
|Chrome_supported=No
|Chrome_version=
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
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
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/Web/CSS/text-indent
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}