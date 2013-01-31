{{Page_Title|background-position}}
{{Flags}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|<code>background-position</code> allows you to set the placement of a <code>background-image</code> on the element it is applied to. <code>background-position</code> generally takes two values, which set the horizontal and vertical position of the background image inside the element.}}
{{CSS Property
|Initial value=0 0
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=Pixel value equivalents
|Animatable=Yes
|CSS object model property=backgroundPosition
|Values={{CSS Property Value
|Data Type=20px 40px
|Description=Any standard CSS units are acceptable as <code>background-position</code> values: px, ems, rems, mm, cm etc. Note that unit values specify the distance the top left corner of the background image is away from the top left corner of the element. For more details on these units, read [[css/units/length|Length units]].
}}{{CSS Property Value
|Data Type=30% 15%
|Description=Percentages are acceptable for <code>background-position</code> values, and specify percentages of the overall width and height of the element in question. Note that percentage values specify the distance the top left corner of the background image is away from the top left corner of the element. For more details on percentages, read [[css/units/numeric|Numeric units]].
}}{{CSS Property Value
|Data Type=left top
|Description=<code>background-position</code> can also be expressed as keywords: left top, top, right top, left, center, right, left bottom, bottom, right bottom. These values do not relate specifically to the position of the top left hand corner of the background image, but rather the overall position of the background image inside the element. So for example, a value of <code>right top</code> will make the background image site flush to the top and right sides of the element it is applied to; the top left corner ''won't'' be positioned at the top right of the element!
}}{{CSS Property Value
|Data Type=30% top
|Description=A combination of different types of value (in this case, percentage then keyword) is allowed.
}}{{CSS Property Value
|Data Type=30%
|Description=If only a single value is included, that is taken as the horizontal value, and the vertical value is set as <code>center</code>.
}}{{CSS Property Value
|Data Type=30% 15%, 40% 80%, 10px 10px
|Description=If you have applied multiple background images to an element, you can give each background image a different position by specifying multiple background position values delimited by commas. The values supplied will cycle so that all images are given a <code>background-position</code>, for example if four background images are specified and only two position values, position 1 will be applied to images 1 and 3, and position 2 to images 2 and 4.
}}{{CSS Property Value
|Data Type=bottom 10px right 15px
|Description=CSS3 includes the new four value <code>background-position</code> syntax, which allows you to choose which sides of the element you are positioning the background image relative to (values 1 and 3), and then the distance away from those sides (values 2 and 4). So this example says that you want to position the background image 10 pixels from the bottom of the element, and 15 pixels from the right. If you miss out one of the offset values, the other is assumed to be 0.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=A simple set of five divs.
|Code=&lt;div class="one"&gt;One&lt;/div&gt;
&lt;div class="two"&gt;Two&lt;/div&gt;
&lt;div class="three"&gt;Three&lt;/div&gt;
&lt;div class="four"&gt;Four&lt;/div&gt;
&lt;div class="five"&gt;Five&lt;/div&gt;
}}{{Single Example
|Language=CSS
|Description=This CSS applies the same background image and basic styling to each div, but then each div is given a different background position to vary where the background image is placed.
|Code=div {
  background-image: url(images/icon.png);
  background-repeat: no-repeat;
  font-family: sans-serif;
  font-size: 16px;
  letter-spacing: -1px;
  width: 200px;
  height: 100px;
  margin-right: 10px;
  border: 1px solid #aaa;
  float: left;
  line-height: 100px;
  text-align: center;
  border-radius: 10px;
  text-transform: uppercase;
  text-shadow: 1px 1px 1px black;
  box-shadow: 2px 2px 5px #ccc;
  padding-top: 2px;
}

 
.one {
  background-position: top left; /* positioned at the top left of the element */
}

.two {
  background-position: 2rem 1rem; /* positioned 2rems from the left of the element, and 1rem from the top */
}

.three {
  background-position: 40% 80%; /* positioned 40% of the element's width away from the left side, and 80% of the element's height down from the top */
}

.four {
  background-position: 30px; /* positioned 30px from the left of the element, and vertically centered (the assumed value when no second value is specified) */
}

.five {
  background-position: bottom 30px right 50px; /* positioned 30px from the bottom of the element and 50px from the right */
}
|LiveURL=http://chrisdavidmills.github.com/basic-background-position/
}}{{Single Example
|Language=HTML
|Description=An outer container div with several inner divs.
|Code=&lt;div id="outer"&gt;
    &lt;div id="save"&gt;&lt;/div&gt;
    &lt;div id="settings"&gt;&lt;/div&gt;
    &lt;div id="people"&gt;&lt;/div&gt;
    &lt;div id="search"&gt;&lt;/div&gt;
    &lt;div id="cancel"&gt;&lt;/div&gt;
    &lt;div id="ok"&gt;&lt;/div&gt;
    &lt;div id="back"&gt;&lt;/div&gt;
    &lt;div id="forward"&gt;&lt;/div&gt;
  &lt;/div&gt;
}}{{Single Example
|Language=CSS
|Description=Every inner div is given the same basic styling, and has the same background image applied to it. Each individual div is then given different top and left values to position it in a different place, and a different background-position value to display a different sprite. Each sprite is 128 x 128 px, and the inners divs are set to 128 x 128 px in size, so only a single sprite will be displayed at once by each of them. You need to get the background positions right, so that a whole sprite is displayed, not	a part of two sprites.
|Code=body > div { /* Basic styling for the outer container div */
  width: 1024px;
  height: 640px;
  margin : 5rem auto;
  background: -webkit-linear-gradient(top right, rgba(0,0,0,0),rgba(0,0,0,0.4));
  background: -moz-linear-gradient(top right, rgba(0,0,0,0),rgba(0,0,0,0.4));
  background: -ms-linear-gradient(top right, rgba(0,0,0,0),rgba(0,0,0,0.4));
  background: -o-linear-gradient(top right, rgba(0,0,0,0),rgba(0,0,0,0.4));
  background: linear-gradient(top right, rgba(0,0,0,0),rgba(0,0,0,0.4));
  background-color: #ccc;
  border-radius: 64px;
  box-shadow: 0px 0px 30px black;
  position: relative;
}
	  
div div { /* all the inner divs are given the same width and height, background image, and absolute positioning */
  width: 128px;
  height: 128px;
  position: absolute;
  background: url(sprites.png);
}
	  
#save { /* each individual div is then given different top and left values to position it in a different place,
                  and a different background-position value to display a different sprite. Each sprite is 128 x 128 px, and 
	the inners divs are set to 128 x 128 px in size, so only a single sprite will be displayed at once by
	each of them. You need to get the background positions right, so that a whole sprite is displayed, not
	a part of two sprites  */
  top: 64px;
  left: 64px;
  background-position: 0px 0px;
}
	  
#settings {
  top: 192px;
  left: 192px;
  background-position: -128px 0px;
}

#people {
  top: 320px;
  left: 448px;
  background-position: -256px 0px;
}

#search {
  top: 320px;
  left: 64px;
  background-position: -384px 0px;
}

#cancel {
  top: 448px;
  left: 576px;
  background-position: -512px 0px;
}

#ok {
  top: 448px;
  left: 704px;
  background-position: -640px 0px;
}

#back {
  top: 192px;
  left: 832px;
  background-position: -768px 0px;
}

#forward {
  top: 320px;
  left: 832px;
  background-position: -896px 0px;
}
|LiveURL=http://chrisdavidmills.github.com/css-sprites-example/
}}
}}
{{Notes_Section
|Usage=* <code>background-position</code> has good support across browsers. Be aware however that some [[css/units/length|CSS units]] are recent additions to the language and are there not supported across older browsers.
* CSS sprites is a very common technique used to display multiple small images on a web page while cutting down on file size and HTTP requests. The images in question are all stored in a single image file which is applied to multiple different elements on the page; different parts of that file are then displayed by varying the <code>background-position</code> values. See example 2 for this in action.
* The four value syntax is not supported very widely across browsers.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS 2.1 Colors and Backgrounds
|URL=http://www.w3.org/TR/CSS2/colors.html
|Status=W3C Recommendation
}}{{Related Specification
|Name=CSS Backgrounds and Borders Module Level 3
|URL=http://www.w3.org/TR/css3-background/#background-position
|Status=W3C Candidate Recommendation
|Relevant_changes=Can support multiple background positions, for multiple background images; CSS3 also includes new four-value background position syntax (see Values section).
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=Basic support
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.0 (1.7 or earlier)
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=4.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=3.5
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0 (85)
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=Multiple Backgrounds
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=3.6 (1.9.2)
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=10.5
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.3 (312)
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=Four-value syntax (support for offsets from any edge)
|Chrome_supported=Yes
|Chrome_version=25
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=13.0 (13.0)
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=10.5
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Feature=Basic support
|Android_supported=Yes
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=1.0 (1)
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}{{Compatibility Table Mobile Row
|Feature=Multiple backgrounds
|Android_supported=Unknown
|Android_version=
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=1.0 (1.9.2)
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Unknown
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}{{Compatibility Table Mobile Row
|Feature=Four-value syntax (support for offsets from any edge)
|Android_supported=No
|Android_version=
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=25
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=13.0 (13.0)
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=9.0
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Background
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
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809 Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}