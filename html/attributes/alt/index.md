{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The '''alt''' attribute is used as a textual representation for graphics and buttons in browsers that don't or can't render images, or when the resource is not found.}}
{{Markup_Attribute
|Applies_to=[[dom/HTMLImageElement|HTMLImageElement]]
|Property_applies_to=dom/HTMLElement
|Content=The '''alt''' attribute is required for [[html/elements/img|images]] and [[html/elements/input/image|image buttons]]. It should provide a concise and accurate label representing the image, in case that a user is visually disabled, is using browser that doesn’t render images or can’t receive images due to network errors. If no alt attribute is given, a screen reader can only read “image” or the file name, which is especially bad if the image is the sole content of a link. 

The alt text should be useful in the context it’s displayed. Which alt text is useful, depends on the function of the image on the page. The content of an alt attribute should use general, non-visual language to accommodate non visual users. For example, a picture of a lake intended to evoke an emotion should have text more descriptive than "Lake" or "Clear, blue lake". "Breathtaking open lake" may be more appropriate.

If an image is not intended to be part of the content of the page, but instead is purely decorative, the alt text can be an empty string. This case could apply for an image used as a border or spacing element or if the image is redundantly described in “regular” text on the page.

If the image contains (non-decorative) text, that text should be in the alternative text in full.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=In this example the images provice important information. The alt text therefore needs to convey the same content.
|Code=<p>We accept the these credit cards:</p>
<ul>
   <li><img src="visa.png" alt="Visa"></li>
   <li><img src="americanexpress.png" alt="American Express"></li>
</ul>
|LiveURL=
}}{{Single Example
|Language=HTML
|Description=Depending on the context, the alt text can be short and simple or more descriptive:
|Code=<!-- A photo of the Capitol Office is included to illustrate a political news article: -->
<img src="capitol.jpg" alt="The Capitol">

<!-- A photo of the Capitol Office is included to illustrate an essay about architecture: -->
<img src="capitol.jpg" alt="Capital Dome in neo Classical style. Dome is white, circular with narrow windows on many levels and pillars on the lowest level.">
|LiveURL=
}}{{Single Example
|Language=HTML
|Description=This example shows a decorative use of an image:
|Code=<img src="border.png" alt="">
|LiveURL=
}}{{Single Example
|Language=HTML
|Description=This example shows a redundant image in a link:
|Code=<a href="crocuspage.html">
	<img src="crocus.jpg" alt="">
	<strong> Crocus bulbs</strong>
</a>
|LiveURL=
}}{{Single Example
|Language=HTML
|Description=This example shows a image that is used as a functional icon. A non-empty alt text is mandatory in such cases.
|Code=<a href="javascript:print()">
	<img src="print.png" alt="Print this page">
</a>
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
|Name=HTML5
|URL=http://www.w3.org/TR/html5/embedded-content-0.html#alt
|Status=Proposed Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Topic_clusters=HTML
|Manual_links=Other attributes that can convey alternative text or longer descriptions:

* [[aria/attributes/aria-label]]
* [[aria/attributes/aria-labelledby]]

* [[html/attributes/longDesc]]
* [[aria/attributes/aria-describedby]]
|External_links=* [http://www.w3.org/WAI/tutorials/images/ W3C WAI Web Accessibility Tutorial on Images]
* [http://www.w3.org/WAI/tutorials/images/decision-tree/ W3C WAI Web Accessibility Tutorial '''alt decision tree''']
* http://www.w3.org/TR/2012/WD-html-alt-techniques-20120329/#secm1
* http://www.w3.org/TR/html5/forms.html#attr-input-alt
|Manual_sections=
}}
{{Topics|Accessibility, HTML, Media, Usability}}
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
|Chrome_version=Beta
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=3
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=3
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=0.8
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=1
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=6
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=Beta
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=14
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=2
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=3
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_version=Beta
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=3
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}