{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The '''alt''' attribute is used as a textual representation for graphics and buttons in browsers that don't or can't render images, or when the resource is not found.}}
{{Markup_Attribute
|Applies_to=[[dom/HTMLImageElement|HTMLImageElement]]
|Property_applies_to=dom/HTMLElement
|Content=The '''alt''' tag is required for [[html/elements/img|images]] and [[html/elements/input/image|image buttons]]. It should provide a concise label for the element it is being applied to, for the case that a user is visually disabled or is using browser that doesn't render images.

The alt tag text should be displayed in place of the image if the resource is not found.

For images, it should describe what the image represents. The contents of an alt tag should use general, non-visual language to accommodate non visual users. For example, a picture of a lake intended to evoke an emotion should have text more descriptive than "Lake" or "Clear, blue lake". "Breathtaking open lake" may be more appropriate.

If an image is not intended to be part of the content of the page, but instead is purely functional or aesthetic, the alt text can be an empty string. This case could apply for an image used as a border or spacing element.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the 'alt' attribute to indicate that the icon displayed denotes a read/write property.
|Code=<!doctype html>
<title>Image alt attribute usage</title>
<img src="http://example.com/path/to/no.jpg" alt="No image, so here is the alt text">
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
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
{{See_Also_Section
|External_links=* http://www.w3.org/TR/2012/WD-html-alt-techniques-20120329/#secm1
* http://www.w3.org/TR/html5/forms.html#attr-input-alt
}}
{{Topics|Accessibility, HTML, Media, Usability}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}