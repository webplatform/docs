---
title: 'img'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/7283804'
  - 'http://gist.github.com/65430bc99e5bf2659454'
compatibility:
  feature: img
  topic: html
notes:
  - "The text could use a lot of editing.\nAdd Category, Parent, Children and Compatibility information.\n\n\"Text that has been rendered to a graphic for typographical effect\": Overview CSS text-replacement techniques"
  - 'Require manual conversion! See https://github.com/webplatform/mediawiki-conversion/issues/24'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLImageElement](/dom/HTMLImageElement)'
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
summary: 'The img element (&lt;img&gt;) embeds an image in a document.'
tags:
  - Markup_Elements
  - Graphics
  - HTML
uri: html/elements/img

---
<p>
</p>
<h2>Summary</h2>
<p>
The img element (&amp;lt;img&amp;gt;) embeds an image in a document.</p><p><br/></p>
<h2>Overview Table</h2>

<dl><dt><a href="/dom/interface"> DOM Interface</a></dt>
  <dd><a href="/dom/HTMLImageElement">HTMLImageElement</a></dd>
</dl><p>The <b>img</b> element (&lt;img&gt;) embeds an image in a document, identified by the <b>src</b> attribute. The value of the <b>alt</b> attribute provides equivalent content for those who cannot process images or who have image loading disabled. Any image can be used (png, jpeg, SVG, pdf, EXR, ...), provided the user-agent's ability to process the format.
</p><p>The &lt;img&gt; element can be nested in an <a href="/html/elements/a">&lt;a&gt;</a> element to create an image that links to another page or section.
</p><p>Alternatives to the &lt;img&gt; element include setting the background-image property of an element.
</p>
<h3>Attributes</h3>
<dl><dt> <a href="/html/attributes/alt">alt</a> </dt>
<dd> Description of image contents</dd>
<dt> <a href="/html/attributes/longdesc">longdesc</a> </dt>
<dd> Link to description of image contents</dd>
<dt> <a href="/html/attributes/src_(input,_img)">src</a> </dt>
<dd> Link to image contents</dd>
<dt> <a href="/html/attributes/srcset">srcset</a></dt>
<dt> <a href="/html/attributes/sizes">sizes</a> </dt>
<dd> Specify alternate resolutions of the image</dd>
<dt> <a href="/html/attributes/useMap">usemap</a></dt>
<dt> <a href="/html/attributes/isMap">ismap</a> </dt>
<dd> Create a special kind of link</dd>
<dt> <a href="/html/attributes/width_(img,_input_elements)">width</a></dt>
<dt> <a href="/html/attributes/height">height</a> </dt>
<dd> define image dimensions</dd></dl><h3>States</h3>
<p>An img is always in one of the following states:
</p>
<dl><dt>Unavailable</dt>
<dd>The user agent hasn't obtained any image data.</dd>
<dt>Partially available</dt>
<dd>The user agent has obtained some of the image data.</dd>
<dt>Completely available</dt>
<dd>The user agent has obtained all of the image data and at least the image dimensions are available.</dd>
<dt>Broken</dt>
<dd>The user agent has obtained all of the image data that it can, but it cannot even decode the image enough to get the image dimensions (e.g. the image is corrupted, or the format is not supported, or no data could be obtained).</dd></dl><h3>Accessibility</h3>
<p>When an a element that creates a hyperlink, or a button element, has no textual content but contains one or more images, the alt attributes must contain text that together convey the purpose of the link or button.
</p>
<h4>A phrase or paragraph with an alternative graphical representation</h4>
<p>Sometimes something can be more clearly stated in graphical form, for example as a flowchart, a diagram, a graph, or a simple map showing directions. In such cases, an image can be given using the img element, but the lesser textual version must still be given, so that users who are unable to view the image (e.g. because they have a very slow connection, or because they are using a text-only browser, or because they are listening to the page being read out by a hands-free automobile voice Web browser, or simply because they are blind) are still able to understand the message being conveyed.
</p>
<h4>A short phrase or label with an alternative graphical representation</h4>
<p>A document can contain information in iconic form. The icon is intended to help users of visual browsers to recognize features at a glance.
</p><p>In some cases, the icon is supplemental to a text label conveying the same meaning. In those cases, the alt attribute must be present but must be empty.
</p><p><br/></p>
<h4>Text that has been rendered to a graphic for typographical effect</h4>
<p>Sometimes, an image just consists of text, and the purpose of the image is not to highlight the actual typographic effects used to render the text, but just to convey the text itself.
</p><p>In such cases, the alt attribute must be present but must consist of the same text as written in the image itself.
</p>
<pre>
&lt;h1&gt;&lt;img src="earthdayheading.png" alt="Earth Day"/&gt;&lt;/h1&gt;
</pre>
<h4>A graphical representation of some of the surrounding text</h4>
<p>A document can contain information in iconic form. The icon is intended to help users of visual browsers to recognize features at a glance.
</p><p>In some cases, the icon is supplemental to a text label conveying the same meaning. In those cases, the alt attribute must be present but must be empty.
</p>
<h4>A purely decorative image that doesn't add any information</h4>
<p>In general, if an image is decorative but isn't especially page-specific, for example an image that forms part of a site-wide design scheme, the image should be specified in the site's CSS, not in the markup of the document.
</p><p>However, a decorative image that isn't discussed by the surrounding text but still has some relevance can be included in a page using the img element. Such images are decorative, but still form part of the content. In these cases, the alt attribute must be present but its value must be the empty string.
</p>
<h4>A group of images that form a single larger picture with no links</h4>
<p>When a picture has been sliced into smaller image files that are then displayed together to form the complete picture again, one of the images must have its alt attribute set as per the relevant rules that would be appropriate for the picture as a whole, and then all the remaining images must have their alt attribute set to the empty string.
</p>
<ul><li>In the following example, a picture representing a company logo for W3C has been split into two pieces, the first containing the letters "W3" and the second with the word "C". The alternative text ("W3C") is all in the first image.</li></ul><pre>
&lt;h1&gt;&lt;img src="logo1.png" alt="W3C"&gt;&lt;img src="logo2.png" alt=""/&gt;&lt;/h1&gt;
</pre>
<h4>A group of images that form a single larger picture with links</h4>
<p>Generally, image maps should be used instead of slicing an image for links.
</p><p>However, if an image is indeed sliced and any of the components of the sliced picture are the sole contents of links, then one image per link must have alternative text in its alt attribute representing the purpose of the link.
</p>
<pre>
&lt;p&gt;
  &lt;a href="?go=left" &gt;&lt;img src="fsm-left.png"  alt="Left side. "&gt;&lt;/a&gt;
  &lt;img src="fsm-middle.png" alt=""/&gt;
  &lt;a href="?go=right"&gt;&lt;img src="fsm-right.png" alt="Right side."&gt;&lt;/a&gt;
&lt;/p&gt;
</pre>
<h4>A key part of the content</h4>
<p>In some cases, the image is a critical part of the content. This could be the case, for instance, on a page that is part of a photo gallery. The image is the whole point of the page containing it.
</p><p>How to provide alternative text for an image that is a key part of the content depends on the image's provenance.
</p><p><br/></p>
<ul><li>The general case<br/>When it is possible for detailed alternative text to be provided, for example if the image is part of a series of screenshots in a magazine review, or part of a comic strip, or is a photograph in a blog entry about that photograph, text that can serve as a substitute for the image must be given as the contents of the alt attribute.</li></ul><pre>
&lt;img src="sales.gif"
     title="Sales graph"
     alt="From 1998 to 2005, sales increased by the following percentages
     with each year: 624%, 75%, 138%, 40%, 35%, 9%, 21%"/&gt;
</pre>
<ul><li>Images that defy a complete description<br/>In certain cases, the nature of the image might be such that providing thorough alternative text is impractical. For example, the image could be indistinct, or could be a complex fractal, or could be a detailed topographical map.<br/>In these cases, the alt attribute must contain some suitable alternative text, but it may be somewhat brief.</li></ul><pre>
&lt;figure&gt;
 &lt;img src="/commons/a/a7/Rorschach1.jpg" alt="A shape with left-right
 symmetry with indistinct edges, with a small gap in the center, two
 larger gaps offset slightly from the center, with two similar gaps
 under them. The outline is wider in the top half than the bottom
 half, with the sides extending upwards higher than the center, and
 the center extending below the sides."&gt;
 &lt;figcaption&gt;A black outline of the first of the ten cards
 in the Rorschach inkblot test.&lt;/figcaption&gt;
&lt;/figure&gt;
</pre>
<ul><li>Images whose contents are not known<br/>In some unfortunate cases, there might be no alternative text available at all, either because the image is obtained in some automated fashion without any associated alternative text (e.g. a Webcam), or because the page is being generated by a script using user-provided images where the user did not provide suitable or usable alternative text (e.g. photograph sharing sites), or because the author does not himself know what the images represent (e.g. a blind photographer sharing an image on his blog).<br/>In such cases, the alt attribute may be omitted, but one of the following conditions must be met as well:
<ul><li>The title attribute is present and has a non-empty value.</li>
<li>The img element is in a figure element that contains a figcaption element that contains content other than inter-element whitespace, and, ignoring the figcaption element and its descendants, the figure element has no text node descendants other than inter-element whitespace, and no embedded content descendant other than the img element.</li></ul></li></ul><h4>An image not intended for the user</h4>
<p>Generally authors should avoid using img elements for purposes other than showing images.
</p><p>If an img element is being used for purposes other than showing an image, e.g. as part of a service to count page views, then the alt attribute must be the empty string.
</p><p>In such cases, the width and height attributes should both be set to zero.
</p>
<h4>An image in an e-mail or private document intended for a specific person who is known to be able to view images</h4>
<p>When an image is included in a private communication (such as an HTML e-mail) aimed at a specific person who is known to be able to view images, the alt attribute may be omitted. However, even in such cases it is strongly recommended that alternative text be included (as appropriate according to the kind of image involved, as described in the above entries), so that the e-mail is still usable should the user use a mail client that does not support images, or should the document be forwarded on to other users whose abilities might not include easily seeing images.
</p>
<h2>History</h2>
<p>The <b>img</b> tag was proposed and implemented around 1993: <a rel="nofollow" class="external autonumber" href="http://1997.webhistory.org/www.lists/www-talk.1993q1/0182.html">[1]</a>
</p>
<h2>Examples</h2>
<p>The following example shows how to use the <b>img</b> element to embed an image on a page with an <b>alt</b> attribute to specify text to display if the image isn't able to be displayed.
</p>
<div class="example">
<pre class="html">
&lt;p&gt;
  You are standing in an open field west of a house.
  &lt;img src="house.jpeg" alt="The house is white, with a boarded front door."/&gt;
  There is a small mailbox here.
&lt;/p&gt;

</pre>
<p><a rel="nofollow" class="external text" href="http://gist.github.com/7283804">View live example</a>
</p>
</div>
<p>The following example shows how to use the <b>srcset</b> and <b>sizes</b> attributes to create responsive images. The browser will select the best image depending on viewport width.
</p>
<div class="example">
<pre class="html">
&lt;img sizes="100vw, (min-width:600px) 50vw" srcset="small.jpg 300w, medium.jpg 500w, large.jpg 700w" alt="The house is white, with a boarded front door."/&gt;

</pre>
<p><a rel="nofollow" class="external text" href="http://gist.github.com/65430bc99e5bf2659454">View live example</a>
</p>
</div>
<p>Here a user is asked to pick his preferred color from a list of three. Each color is given by an image, but for users who have configured their user agent not to display images, the color names are used instead:
</p>
<div class="example">
<pre class="html">

&lt;h1&gt;Pick your color&lt;/h1&gt;
&lt;ul&gt;
  &lt;li&gt;&lt;a href="green.html"&gt;&lt;img src="green.jpeg" alt="Green"/&gt;&lt;/a&gt;&lt;/li&gt;
  &lt;li&gt;&lt;a href="blue.html"&gt;&lt;img src="blue.jpeg" alt="Blue"/&gt;&lt;/a&gt;&lt;/li&gt;
  &lt;li&gt;&lt;a href="red.html"&gt;&lt;img src="red.jpeg" alt="Red"/&gt;&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;


</pre>
<p><br/></p>
</div>
<p>In the following example we have a flowchart in image form, with text in the alt attribute rephrasing the flowchart in prose form. (The alt-text is a replacement for the image, not a description of the image.)
</p>
<div class="example">
<pre class="html">

&lt;p&gt;In the common case, the data handled by the tokenization stage
comes from the network, but it can also come from script.&lt;/p&gt;
&lt;p&gt;&lt;img src="images/parsing-model-overview.png" alt="The network
passes data to the Tokenizer stage, which passes data to the Tree
Construction stage. From there, data goes to both the DOM and to
Script Execution. Script Execution is linked to the DOM, and, using
document.write(), passes data to the Tokenizer."/&gt;&lt;/p&gt;


</pre>
<p><br/></p>
</div>
<p><br/></p><p><br/></p>
<h2>Related specifications</h2>

<dl><dt><a rel="nofollow" class="external text" href="http://www.w3.org/TR/html51/embedded-content.html#the-img-element">HTML 5.1</a></dt>
  <dd>W3C Working Draft</dd>
</dl><dl><dt><a rel="nofollow" class="external text" href="http://www.w3.org/TR/html5/embedded-content-0.html#the-img-element">HTML 5</a></dt>
  <dd>W3C Recommendation</dd>
</dl><dl><dt><a rel="nofollow" class="external text" href="http://www.w3.org/TR/html401/struct/objects.html#edef-IMG">HTML 4.01</a></dt>
  <dd>W3C Recommendation</dd>
</dl><h2>See also</h2>
<h3>Related articles</h3>
<h4>HTML</h4>
<ul><li> <a href="/css/properties/user-modify">user-modify</a></li></ul><p><br/></p>
<ul><li> <a href="/dom/HTMLTextAreaElement/textLength">textLength</a></li></ul><p><br/></p>
<ul><li> <a href="/dom/HTMLTextAreaElement/value">value</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/accept">accept</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/action">action</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/alt">alt</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/autocomplete">autocomplete</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/autofocus">autofocus</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/checked">checked</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/crossorigin">crossorigin</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/form">form</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/formEnctype">formEnctype</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/height">height</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/list">list</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/max_(HTMLInputElement)">max (HTMLInputElement)</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/maxLength">maxLength</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/min">min</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/multiple">multiple</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/readonly">readonly</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/size">size</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/standby">standby</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/step">step</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements">HTML Elements</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/!DOCTYPE">!DOCTYPE</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/!DOCTYPE/ja">!DOCTYPE</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/acronym">acronym</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/b">b</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/b/ja">b</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/br">br</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/br/ja">br</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/button">button</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/button/ja">button</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/caption">caption</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/cite">cite</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/code">code</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/col">col</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/colgroup">colgroup</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/datalist">datalist</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/del">del</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/dfn">dfn</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/div">div</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/em">em</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/embed">EMBED</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/fieldset">fieldset</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/font">font</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/footer">footer</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/head">head</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/hn">hn</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/hr">hr</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/html">html</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/i">i</a></li></ul><p><br/></p>
<ul><li> <strong class="selflink">img</strong></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/input">input</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/ins">ins</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/kbd">kbd</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/legend">legend</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/mark">mark</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/option">option</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/p">p</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/samp">samp</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/script">script</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/span">span</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/strong">strong</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/table">table</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/tbody">tbody</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/td">td</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/tfoot">tfoot</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/th">th</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/time">time</a></li></ul><h4>Multimedia</h4>
<ul><li> <a href="/apis/MediaStream/ended">Track ended</a></li></ul><p><br/></p>
<ul><li> <a href="/apis/media_source_extensions/MediaSource">MediaSource</a></li></ul><p><br/></p>
<ul><li> <a href="/apis/media_source_extensions/MediaSource/appendBuffer">appendBuffer</a></li></ul><p><br/></p>
<ul><li> <a href="/concepts/Internet_and_Web/webrtc">WebRTC</a></li></ul><p><br/></p>
<ul><li> <a href="/css/properties/object-fit">object-fit</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/height">height</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/standby">standby</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/embed">EMBED</a></li></ul><p><br/></p>
<ul><li> <strong class="selflink">img</strong></li></ul><p><br/></p>
<ul><li> <a href="/tutorials/webrtc_resources">WebRTC Resources</a></li></ul><p><br/></p>
<h3>External resources</h3>
<ul><li><a rel="nofollow" class="external free" href="http://www.w3.org/wiki/HTML/Elements/img">http://www.w3.org/wiki/HTML/Elements/img</a></li>
<li><a rel="nofollow" class="external text" href="http://scottjehl.github.io/picturefill/">Picturefill is a polyfill to support srcset and sizes attributes</a></li></ul>
