{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add Category, Parent, Children and Compatibility information. Add HTML information section.
|Checked_Out=No
|Content=Compatibility Incomplete
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The '''img''' element <nowiki>(<img>)</nowiki> embeds an image in a document.}}
{{Markup_Element
|DOM_interface=dom/HTMLImageElement
|Content=The '''img''' element (&lt;img&gt;) embeds an image in a document. The &lt;img&gt; element can be nested in an [[html/elements/a|&lt;a&gt;]] element to create an image that links to another page or section. The value of the '''alt''' attribute provides equivalent content for those who cannot process images or who have image loading disabled.  Alternatives to the &lt;img&gt; element include setting the background-image property of an element.

===Attributes===
*[http://docs.webplatform.org/wiki/html/attributes/alt alt]
*[http://docs.webplatform.org/wiki/html/attributes/src_(input,_img) src]
*[http://docs.webplatform.org/wiki/html/attributes/srcset srcset]
*[http://docs.webplatform.org/wiki/html/attributes/sizes sizes]
*[http://docs.webplatform.org/wiki/html/attributes/useMap usemap]
*[http://docs.webplatform.org/wiki/html/attributes/isMap ismap]
*[http://docs.webplatform.org/wiki/html/attributes/width_(img,_input_elements) width]
*[http://docs.webplatform.org/wiki/html/attributes/height height]

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
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following example shows how to use the '''img''' element to embed an image on a page with an '''alt''' attribute to specify text to display if the image isn't able to be displayed.
|Code=<p>
  You are standing in an open field west of a house.
  <img src="house.jpeg" alt="The house is white, with a boarded front door.">
  There is a small mailbox here.
</p>
|LiveURL=http://code.webplatform.org/gist/7283804
}}{{Single Example
|Language=HTML
|Description=The following example shows how to use the '''srcset''' and '''sizes''' attributes to create responsive images. The browser will select the best image depending on viewport width.
|Code=<img sizes="100vw, (min-width:600px) 50vw" srcset="small.jpg 300w, medium.jpg 500w, large.jpg 700w" alt="The house is white, with a boarded front door.">
|LiveURL=http://code.webplatform.org/gist/65430bc99e5bf2659454
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 2.0
|URL=http://www.w3.org/MarkUp/html-spec/html-spec_5.html#SEC5.10
|Status=W3C Recommendation
}}{{Related Specification
|Name=HTML5
|URL=http://www.w3.org/TR/html5/embedded-content-0.html#the-img-element
|Status=W3C Candidate Recommendation
}}{{Related Specification
|Name=srcset
|URL=http://www.w3.org/html/wg/drafts/srcset/w3c-srcset/
|Status=W3C Editor’s Draft
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
{{See_Also_Section
|Topic_clusters=HTML, Multimedia
|External_links=*http://www.w3.org/wiki/HTML/Elements/img
*[http://scottjehl.github.io/picturefill/ Picturefill is a polyfill to support srcset and sizes attributes]
}}
{{Topics|Graphics, HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}