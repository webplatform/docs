{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=The text could use a lot of editing.
Add Category, Parent, Children and Compatibility information.

"Text that has been rendered to a graphic for typographical effect": Overview CSS text-replacement techniques
|Checked_Out=No
|Content=Compatibility Incomplete
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The '''img''' element <nowiki>(<img>)</nowiki> embeds an image in a document.}}
{{Markup_Element
|DOM_interface=dom/HTMLImageElement
|Tag_omissions=
|CSS_display=
|Content=The '''img''' element (&lt;img&gt;) embeds an image in a document, identified by the '''src''' attribute. The value of the '''alt''' attribute provides equivalent content for those who cannot process images or who have image loading disabled. Any image can be used (png, jpeg, SVG, pdf, EXR, ...), provided the user-agent's ability to process the format.

The &lt;img&gt; element can be nested in an [[html/elements/a|&lt;a&gt;]] element to create an image that links to another page or section.

Alternatives to the &lt;img&gt; element include setting the background-image property of an element.

===Attributes===
; [[html/attributes/alt|alt] : Description of image contents
; [[html/attributes/longdesc|longdesc] : Link to description of image contents
; [[html/attributes/src_(input,_img)|src] : Link to image contents
; [[html/attributes/srcset|srcset]
; [[html/attributes/sizes|sizes] : Specify alternate resolutions of the image
; [[html/attributes/useMap|usemap]
; [[html/attributes/isMap|ismap] : Create a special kind of link
; [[html/attributes/width_(img,_input_elements)|width]
; [[html/attributes/height|height] : define image dimensions

===States===
An img is always in one of the following states:
;Unavailable
:The user agent hasn't obtained any image data.
;Partially available
:The user agent has obtained some of the image data.
;Completely available
:The user agent has obtained all of the image data and at least the image dimensions are available.
;Broken
:The user agent has obtained all of the image data that it can, but it cannot even decode the image enough to get the image dimensions (e.g. the image is corrupted, or the format is not supported, or no data could be obtained).

===Accessibility===
When an a element that creates a hyperlink, or a button element, has no textual content but contains one or more images, the alt attributes must contain text that together convey the purpose of the link or button.

==== A phrase or paragraph with an alternative graphical representation ====
Sometimes something can be more clearly stated in graphical form, for example as a flowchart, a diagram, a graph, or a simple map showing directions. In such cases, an image can be given using the img element, but the lesser textual version must still be given, so that users who are unable to view the image (e.g. because they have a very slow connection, or because they are using a text-only browser, or because they are listening to the page being read out by a hands-free automobile voice Web browser, or simply because they are blind) are still able to understand the message being conveyed.

==== A short phrase or label with an alternative graphical representation ====
A document can contain information in iconic form. The icon is intended to help users of visual browsers to recognize features at a glance.

In some cases, the icon is supplemental to a text label conveying the same meaning. In those cases, the alt attribute must be present but must be empty.


==== Text that has been rendered to a graphic for typographical effect ====
Sometimes, an image just consists of text, and the purpose of the image is not to highlight the actual typographic effects used to render the text, but just to convey the text itself.

In such cases, the alt attribute must be present but must consist of the same text as written in the image itself.
<pre>
<h1><img src="earthdayheading.png" alt="Earth Day"/></h1>
</pre>

==== A graphical representation of some of the surrounding text ====
A document can contain information in iconic form. The icon is intended to help users of visual browsers to recognize features at a glance.

In some cases, the icon is supplemental to a text label conveying the same meaning. In those cases, the alt attribute must be present but must be empty.

==== A purely decorative image that doesn't add any information ====
In general, if an image is decorative but isn't especially page-specific, for example an image that forms part of a site-wide design scheme, the image should be specified in the site's CSS, not in the markup of the document.

However, a decorative image that isn't discussed by the surrounding text but still has some relevance can be included in a page using the img element. Such images are decorative, but still form part of the content. In these cases, the alt attribute must be present but its value must be the empty string.

==== A group of images that form a single larger picture with no links  ====
When a picture has been sliced into smaller image files that are then displayed together to form the complete picture again, one of the images must have its alt attribute set as per the relevant rules that would be appropriate for the picture as a whole, and then all the remaining images must have their alt attribute set to the empty string.

*In the following example, a picture representing a company logo for W3C has been split into two pieces, the first containing the letters "W3" and the second with the word "C". The alternative text ("W3C") is all in the first image.
<pre>
<h1><img src="logo1.png" alt="W3C"><img src="logo2.png" alt=""/></h1>
</pre>

==== A group of images that form a single larger picture with links ====
Generally, image maps should be used instead of slicing an image for links.

However, if an image is indeed sliced and any of the components of the sliced picture are the sole contents of links, then one image per link must have alternative text in its alt attribute representing the purpose of the link.
<pre>
<p>
  <a href="?go=left" ><img src="fsm-left.png"  alt="Left side. "></a>
  <img src="fsm-middle.png" alt=""/>
  <a href="?go=right"><img src="fsm-right.png" alt="Right side."></a>
</p>
</pre>

==== A key part of the content ====
In some cases, the image is a critical part of the content. This could be the case, for instance, on a page that is part of a photo gallery. The image is the whole point of the page containing it.

How to provide alternative text for an image that is a key part of the content depends on the image's provenance.


*The general case<br />When it is possible for detailed alternative text to be provided, for example if the image is part of a series of screenshots in a magazine review, or part of a comic strip, or is a photograph in a blog entry about that photograph, text that can serve as a substitute for the image must be given as the contents of the alt attribute.
<pre>
<img src="sales.gif"
     title="Sales graph"
     alt="From 1998 to 2005, sales increased by the following percentages
     with each year: 624%, 75%, 138%, 40%, 35%, 9%, 21%"/>
</pre>

*Images that defy a complete description<br />In certain cases, the nature of the image might be such that providing thorough alternative text is impractical. For example, the image could be indistinct, or could be a complex fractal, or could be a detailed topographical map.<br />In these cases, the alt attribute must contain some suitable alternative text, but it may be somewhat brief.
<pre>
<figure>
 <img src="/commons/a/a7/Rorschach1.jpg" alt="A shape with left-right
 symmetry with indistinct edges, with a small gap in the center, two
 larger gaps offset slightly from the center, with two similar gaps
 under them. The outline is wider in the top half than the bottom
 half, with the sides extending upwards higher than the center, and
 the center extending below the sides.">
 <figcaption>A black outline of the first of the ten cards
 in the Rorschach inkblot test.</figcaption>
</figure>
</pre>

*Images whose contents are not known<br />In some unfortunate cases, there might be no alternative text available at all, either because the image is obtained in some automated fashion without any associated alternative text (e.g. a Webcam), or because the page is being generated by a script using user-provided images where the user did not provide suitable or usable alternative text (e.g. photograph sharing sites), or because the author does not himself know what the images represent (e.g. a blind photographer sharing an image on his blog).<br />In such cases, the alt attribute may be omitted, but one of the following conditions must be met as well:
**The title attribute is present and has a non-empty value.
**The img element is in a figure element that contains a figcaption element that contains content other than inter-element whitespace, and, ignoring the figcaption element and its descendants, the figure element has no text node descendants other than inter-element whitespace, and no embedded content descendant other than the img element.

==== An image not intended for the user ====
Generally authors should avoid using img elements for purposes other than showing images.

If an img element is being used for purposes other than showing an image, e.g. as part of a service to count page views, then the alt attribute must be the empty string.

In such cases, the width and height attributes should both be set to zero.

==== An image in an e-mail or private document intended for a specific person who is known to be able to view images ====
When an image is included in a private communication (such as an HTML e-mail) aimed at a specific person who is known to be able to view images, the alt attribute may be omitted. However, even in such cases it is strongly recommended that alternative text be included (as appropriate according to the kind of image involved, as described in the above entries), so that the e-mail is still usable should the user use a mail client that does not support images, or should the document be forwarded on to other users whose abilities might not include easily seeing images.

== History ==

The '''img''' tag was proposed and implemented around 1993: [http://1997.webhistory.org/www.lists/www-talk.1993q1/0182.html]
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following example shows how to use the '''img''' element to embed an image on a page with an '''alt''' attribute to specify text to display if the image isn't able to be displayed.
|Code=<p>
  You are standing in an open field west of a house.
  <img src="house.jpeg" alt="The house is white, with a boarded front door."/>
  There is a small mailbox here.
</p>
|LiveURL=http://code.webplatform.org/gist/7283804
}}{{Single Example
|Language=HTML
|Description=The following example shows how to use the '''srcset''' and '''sizes''' attributes to create responsive images. The browser will select the best image depending on viewport width.
|Code=<img sizes="100vw, (min-width:600px) 50vw" srcset="small.jpg 300w, medium.jpg 500w, large.jpg 700w" alt="The house is white, with a boarded front door."/>
|LiveURL=http://code.webplatform.org/gist/65430bc99e5bf2659454
}}{{Single Example
|Language=HTML
|Description=Here a user is asked to pick his preferred color from a list of three. Each color is given by an image, but for users who have configured their user agent not to display images, the color names are used instead:
|Code=<nowiki>
<h1>Pick your color</h1>
<ul>
  <li><a href="green.html"><img src="green.jpeg" alt="Green"/></a></li>
  <li><a href="blue.html"><img src="blue.jpeg" alt="Blue"/></a></li>
  <li><a href="red.html"><img src="red.jpeg" alt="Red"/></a></li>
</ul>
</nowiki>
|LiveURL=
}}{{Single Example
|Language=HTML
|Description=In the following example we have a flowchart in image form, with text in the alt attribute rephrasing the flowchart in prose form. (The alt-text is a replacement for the image, not a description of the image.)
|Code=<nowiki>
<p>In the common case, the data handled by the tokenization stage
comes from the network, but it can also come from script.</p>
<p><img src="images/parsing-model-overview.png" alt="The network
passes data to the Tokenizer stage, which passes data to the Tree
Construction stage. From there, data goes to both the DOM and to
Script Execution. Script Execution is linked to the DOM, and, using
document.write(), passes data to the Tokenizer."/></p>
</nowiki>
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
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/embedded-content.html#the-img-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/embedded-content-0.html#the-img-element
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/objects.html#edef-IMG
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Topic_clusters=HTML, Multimedia
|Manual_links=
|External_links=*http://www.w3.org/wiki/HTML/Elements/img
*[http://scottjehl.github.io/picturefill/ Picturefill is a polyfill to support srcset and sizes attributes]
|Manual_sections=
}}
{{Topics|Graphics, HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
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
|Internet_explorer_version=1.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=5.12
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=srcset support
|Chrome_supported=Yes
|Chrome_version=34.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=No
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=21.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Chrome
|Version=34.0
|Note=Chrome has implemented srcset with version 34.0 but doesn’t yet support the sizes attribute.
}}
}}