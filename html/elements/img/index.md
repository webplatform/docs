{{Page_Title}}
{{Flags
|Content=Incomplete, Compatibility Incomplete
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The '''img''' element <nowiki>(<img>)</nowiki> represents an image.}}
{{Markup_Element
|DOM_interface=dom/HTMLImageElement
|Content=The '''img''' element (&lt;img&gt;) embeds an image in a document. The &lt;img&gt; element can be nested in an [[html/elements/a|&lt;a&gt;]] element to create an image that links to another page or section. The value of the '''alt''' attribute (&lt;alt&gt;) provides equivalent content for those who cannot process images or who have image loading disabled.  Alternatives to the &lt;img&gt; element include setting the background-image property of an element.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following example shows how to use the '''img''' element to embed an image on a page with an '''alt''' attribute to specify text to display if the image isn't able to be displayed.
|Code=<nowiki>
<p>
  You are standing in an open field west of a house.
  <img src="house.jpeg" alt="The house is white, with a boarded front door.">
  There is a small mailbox here.
</p>
</nowiki>
|LiveURL=http://code.webplatform.org/gist/7283804
}}
}}
{{Notes_Section
|Usage====Attributes===
;alt = Normal character data
: Gives the fallback content for the image.
;src = URL potentially surrounded by spaces
: Specifies a URL referencing a non-interactive, optionally animated, image that is neither paged nor scripted.
;usemap = Hash-name reference
: Specifies a hash-name reference to a map element with which to associate the object.
;ismap = Boolean value
: Specifies that its img element provides access to a server-side image map.
;width = Non-negative integer
: Give the width of the visual content of the element, in CSS pixels.
;height = Non-negative integer
: Give the height of the visual content of the element, in CSS pixels. 

|Notes====Remarks===

}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 2.0
|URL=http://www.w3.org/MarkUp/html-spec/html-spec_5.html#SEC5.10
|Status=W3C Recommendation
}}{{Related Specification
|Name=HTML5
|URL=http://www.w3.org/TR/html5/embedded-content-0.html#the-img-element
|Status=W3C Candidate Recommendation
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
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=HTML, Multimedia
}}
{{Topics|Graphics, HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}