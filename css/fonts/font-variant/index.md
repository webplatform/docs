{{Page_Title|background-image}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Applies one or more background images to an element. These can be any valid CSS image, including url() paths to image files or CSS gradients.}}
{{CSS Property
|Initial value=none
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=As specified, but with URIs made absolute
|Animatable=Yes
|CSS object model property=backgroundImage
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=none
|Description=Default. Color of the next parent through which the background is visible.
}}{{CSS Property Value
|Data Type=<image>
|Description=Any valid CSS image value, including image files through [[css/functions/url()|CSS images: url()]] or CSS gradients.
}}{{CSS Property Value
|Data Type=<image>, <image>, …
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
|Description=The first div has a simple image file applied to it, the second div has a background gradient applied to it, and the third div has both applied simultaneously.
|Code=.one {
  background-image: url(images/icon.png);
  /* here we are applying a single background image to our first block level container element */
  /* (could be anything, but it is a div in the live example. */
}

.two {
  background-image: -webkit-linear-gradient(top, #aaa, #eee);
  background-image: -moz-linear-gradient(top, #aaa, #eee);
  background-image: -ms-linear-gradient(top, #aaa, #eee);
  background-image: -o-linear-gradient(top, #aaa, #eee);
  background-image: linear-gradient(to bottom, #aaa, #eee);
  /* Here we are applying a linear gradient to our second block level container. */
  /* We have included a line with each different vendor prefix type, so that all supporting */
  /* browsers will have something they can apply. This includes a prefixless version of the */
  /* property, which uses the latest version of the syntax for the spec. As browsers update their  */
  /* implementations and drop their prefixes, tyhey can start to use this syntax instead, meaning */
  /* that the code will still work. */  
}

.three {
  background-image: url(images/icon.png), -webkit-linear-gradient(top, #aaa, #eee);
  background-image: url(images/icon.png), -moz-linear-gradient(top, #aaa, #eee);
  background-image: url(images/icon.png), -ms-linear-gradient(top, #aaa, #eee);
  background-image: url(images/icon.png), -o-linear-gradient(top, #aaa, #eee);
  background-image: url(images/icon.png), linear-gradient(to bottom, #aaa, #eee);
  /* In this case we are applying both the background image and the gradient to our third block level container. */
}
|LiveURL=http://chrisdavidmills.github.com/background-image/background-image.html
}}
}}
{{Notes_Section
|Usage=Background images in general have good support across browsers; there are a few things to take note of, however:

* Older browsers do not support multiple background images, SVG as background images or CSS gradients, so be careful when using these options to make sure that a fallback is provided that will make content readable on older browsers, such as a simple solid colour.
* When using multiple background images, the image at the start of the comma delimited list appears on top of ones later on. This might seem contrary to how CSS is expected to behave.
* Because gradients are still supported in some browsers with prefixes and some not, and some with a slightly older syntax, you should use multiple background gradient properties with different syntaxes, as shown in the below examples.
|Notes=Internationalization topics related to the <code>background-image</code> property:
* [http://localhost/International/techniques/authoring-html#textexpansion Preparing for text expansion]
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
|Relevant_changes=Multiple background images can be specified on the same element
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
|Safari_version=1.0
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=Multiple backgrounds
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=3.6
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9.0
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=9.0
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=SVG background images
|Chrome_supported=Yes
|Chrome_version=8.0
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=4.0
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9.0
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=9.5
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=4.0
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=Gradients
|Chrome_supported=No
|Chrome_version=
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=8.0
|Firefox_supported=Yes
|Firefox_version=16.0
|Firefox_prefixed_supported=Yes
|Firefox_prefixed_version=3.6
|Internet_explorer_supported=Yes
|Internet_explorer_version=10.0
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.10
|Opera_prefixed_supported=Yes
|Opera_prefixed_version=11.0
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=Yes
|Safari_prefixed_version=4.0
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=1.0
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=3.8
|Blackberry_prefixed_supported=No
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=18.0
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=1.0
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=6.0
|IE_mobile_prefixed_supported=No
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=7.0
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_version=4.0
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=1.0
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}{{Compatibility Table Mobile Row
|Feature=Multiple backgrounds
|Android_supported=Yes
|Android_version=1.0
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=3.8
|Blackberry_prefixed_supported=No
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=18.0
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=1.0
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=8.0
|IE_mobile_prefixed_supported=No
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=8.5
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_version=5.0
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=1.0
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}{{Compatibility Table Mobile Row
|Feature=SVG background images
|Android_supported=Yes
|Android_version=1.0
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=3.8
|Blackberry_prefixed_supported=No
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=18.0
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=8.0
|IE_mobile_prefixed_supported=No
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=10.0
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_version=6.0
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=1.0
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}{{Compatibility Table Mobile Row
|Feature=Gradients
|Android_supported=No
|Android_version=
|Android_prefixed_supported=Yes
|Android_prefixed_version=1.0
|Blackberry_supported=No
|Blackberry_version=
|Blackberry_prefixed_supported=Yes
|Blackberry_prefixed_version=3.8
|Chrome_mobile_supported=No
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Yes
|Chrome_mobile_prefixed_version=18.0
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=16.0
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=No
|IE_mobile_version=
|IE_mobile_prefixed_supported=Yes
|IE_mobile_prefixed_version=8.0
|Opera_mobile_supported=Yes
|Opera_mobile_version=12.0
|Opera_mobile_prefixed_supported=Yes
|Opera_mobile_prefixed_version=11.0
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Yes
|Safari_mobile_prefixed_version=1.0
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=< 9.0
|Note=Doesn't support SVG for background-images, or multiple background images, or gradients.
}}{{Compatibility Notes Row
|Browser=Internet Explorer
|Version=< 10.0
|Note=Doesn't support gradients.
}}{{Compatibility Notes Row
|Browser=Various
|Note=Not all browsers support animation of background images. Recent WebKit or Blink-based browsers transition between background images by cross fading. (Non standard)
}}
}}
{{See_Also_Section
|Topic_clusters=Background
|Manual_links=* [[tutorials/using_css_background_images|Using CSS background images]]
* [[tutorials/creating_gradients_in_css|Creating gradients in CSS]]
|External_links=* [http://www.netmagazine.com/tutorials/get-grips-css3-multiple-background-images Get to grips with CSS3 multiple background images], by Prisca Schmarsow
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}