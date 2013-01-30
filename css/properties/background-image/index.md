{{Page_Title|background-image}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Cleanup, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Applies background images to HTML elements.}}
{{CSS Property
|Initial value=none
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=As specified, but with URIs made absolute
|Animatable=Yes
|CSS object model property=backgroundImage
|Values={{CSS Property Value
|Data Type=none
|Description=Default. Color of the next parent through which the background is visible.
}}{{CSS Property Value
|Data Type=url(path/to/image.png)
|Description=This value contains a path to an image that you want to apply to the element in question as a background image, using the CSS images syntax, as described at [[css/functions/url()|CSS images: url()]].
}}{{CSS Property Value
|Data Type=linear-gradient(to bottom, #f00, #aaa)
|Description=Programmatically creates a gradient that travels from one side of the element to the other. For more on the syntax, read [[tutorials/creating_gradients_in_css|Creating gradients in CSS]].
}}{{CSS Property Value
|Data Type=radial-gradient(50% 50%, circle, #f00, #aaa)
|Description=Programmatically creates a gradient that radiates outwards from a specified point on the element's background. For more on the syntax, read [[tutorials/creating_gradients_in_css|Creating gradients in CSS]].
}}{{CSS Property Value
|Data Type=url(path/to/image.png), url(path/to/image2.png), url(path/to/image3.png)
|Description=You can apply multiple background images to a single element (image files, gradients, or a mixture) by including all the image references in the property value, with each one separated by a comma. Images referenced earlier in the property value appear in front of images referenced later.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=Three simple div elements
|Code=&lt;!DOCTYPE HTML&gt;
&lt;html lang="en-US"&gt;
&lt;head&gt;
  &lt;meta charset="UTF-8"&gt;
  &lt;title&gt;Background-image example&lt;/title&gt;
  &lt;link href="background-image.css" type="text/css" rel="stylesheet"&gt;
&lt;/head&gt;
&lt;body&gt;

  &lt;div class="one"&gt;One&lt;/div&gt;
  &lt;div class="two"&gt;Two&lt;/div&gt;
  &lt;div class="three"&gt;Three&lt;/div&gt;

&lt;/body&gt;
&lt;/html&gt;
}}{{Single Example
|Language=CSS
|Description=* The first div has a simple image file applied to it.
* The second div has a background gradient applied to it.
* The third div has both applied simultaneously.
|Code=.one {
  background-image: url(images/icon.png);
  /* here we are applying a single background image to our first block level container element */
  /* (could be anything, but it is a div in the live example. */
}

.two {
  background-image: -webkit-linear-gradient(top,#aaa,#eee);
  background-image: -moz-linear-gradient(top,#aaa,#eee);
  background-image: -ms-linear-gradient(top,#aaa,#eee);
  background-image: -o-linear-gradient(top,#aaa,#eee);
  background-image: linear-gradient(to bottom,#aaa,#eee);
  /* Here we are applying a linear gradient to our second block level container. */
  /* We have included a line with each different vendor prefix type, so that all supporting */
  /* browsers will have something they can apply. This includes a prefixless version of the */
  /* property, which uses the latest version of the syntax for the spec. As browsers update their  */
  /* implementations and drop their prefixes, tyhey can start to use this syntax instead, meaning */
  /* that the code will still work. */  
}

.three {
  background-image: url(images/icon.png), -webkit-linear-gradient(top,#aaa,#eee);
  background-image: url(images/icon.png), -moz-linear-gradient(top,#aaa,#eee);
  background-image: url(images/icon.png), -ms-linear-gradient(top,#aaa,#eee);
  background-image: url(images/icon.png), -o-linear-gradient(top,#aaa,#eee);
  background-image: url(images/icon.png), linear-gradient(to bottom,#aaa,#eee);
  /* In this case we are applying both the background image and the gradient to our third block level container. */
}
}}
}}
{{Notes_Section
|Usage=Background images in general have good support across browsers; there are a few things to take note of, however:

* Older browsers do not support multiple background images, SVG as background images or CSS gradients, so be careful when using these options to make sure that a fallback is provided that will make content readable on older browsers, such as a simple solid colour.
* When using multiple background images, the image at the start of the comma delimited list appears on top of ones later on. This might seem contrary to how CSS is expected to behave.
* Because gradients are still supported in some browsers with prefixes and some not, and some with a slightly older syntax, you should use multiple background gradient properties with different syntaxes, as shown in the below examples.
|Notes=The background-image property allows you to apply one or more background images to an element. These can be url() paths to image files, or CSS3 linear or radial gradients. For more information, consult [[tutorials/using_css_background_images|Using CSS background images]] and [[tutorials/creating_gradients_in_css|Creating gradients in CSS]].
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS 2.1
|URL=http://www.w3.org/TR/CSS2/colors.html#propdef-background-image
|Status=W3C Recommendation
}}{{Related Specification
|Name=CSS Backgrounds and Borders Module Level 3
|URL=http://www.w3.org/TR/css3-background/#the-background-image
|Status=W3C Candidate Recommendation
|Relevant_changes=Several overlaid images can be specified
}}
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
|Firefox_version=1.0
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=4.0
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=3.5
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_prefixed_supported=No
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_prefixed_supported=No
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}{{Compatibility Table Mobile Row
|Feature=Data URI
|Android_supported=Yes
|Android_version=4
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
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=10
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
|Safari_mobile_supported=Yes
|Safari_mobile_version=3.2
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=3.0
|Note=Microsoft Internet Explorer 3.0 supports the '''background-image''' attribute, but only when it's set through the [[css/cssom/properties/background|'''background''']] attribute.
}}
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
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}