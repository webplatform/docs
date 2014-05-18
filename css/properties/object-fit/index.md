{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The ''object-fit'' property defines how content of a replaced element (e.g. a video or an image) is made to fit the dimensions of its containing box}}
{{CSS Property
|Initial value=fill
|Applies to=Replaced elements
|Inherited=No
|Media=visual
|Computed value=As specified
|Animatable=No
|CSS object model property=objectFit
|Values={{CSS Property Value
|Data Type=fill
|Description=The replaced content is sized to fill the element's box
}}{{CSS Property Value
|Data Type=contain
|Description=The replaced content is sized to maintain it's aspect ratio while fitting within the element's content box
}}{{CSS Property Value
|Data Type=cover
|Description=The replaced content is sized to maintain it's aspect ratio while filling the element's entire content box
}}{{CSS Property Value
|Data Type=none
|Description=The replaced content is not resized to fit inside the element's content box
}}{{CSS Property Value
|Data Type=scale-down
|Description=Size the content as if ‘none’ or ‘contain’ were specified, whichever would result in a smaller concrete object size
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=Five simple img elements
|Code=&lt;!DOCTYPE HTML&gt;
&lt;html lang="en-US"&gt;
&lt;head&gt;
  &lt;meta charset="UTF-8"&gt;
  &lt;title&gt;Object-fit example&lt;/title&gt;
  &lt;link href="content-fit.css" type="text/css" rel="stylesheet"&gt;
&lt;/head&gt;
&lt;body&gt;

  &lt;img src="http://www.webplatform.org/logo/wplogo_pillow_wide_tan.png" alt="Webplatform Logo" class="fill"/&gt;
  &lt;img src="http://www.webplatform.org/logo/wplogo_pillow_wide_tan.png" alt="Webplatform Logo" class="contain"/&gt;
  &lt;img src="http://www.webplatform.org/logo/wplogo_pillow_wide_tan.png" alt="Webplatform Logo" class="cover"/&gt;
  &lt;img src="http://www.webplatform.org/logo/wplogo_pillow_wide_tan.png" alt="Webplatform Logo" class="none"/&gt;
  &lt;img src="http://www.webplatform.org/logo/wplogo_pillow_wide_tan.png" alt="Webplatform Logo" class="scale-down"/&gt;

&lt;/body&gt;
&lt;/html&gt;
}}{{Single Example
|Language=CSS
|Description=Alle five images are forced to 150x100 pixel, that's different from both the original size of the image (196x77 pixel) and it's aspect ratio. 
|Code=img {
  float: left;
  width: 150px;
  height: 100px;
  border: 1px solid #000;
  margin-right: 1em;
}
.fill {
  object-fit: fill;
  /* This is the default behaviour. The image is forced to fill the whole box, the aspect ratio is ignored. */
}
.contain {
  object-fit: contain;
  /* The whole image will be displayed in the box and scaled down or expanded if necessary. The aspect ratio is maintained. */
}
.cover {
  object-fit: cover;
  /* The whole image is scaled down or expanded till it fills the box completely, the aspect ratio is maintained. This normally results in only part of the image being visible. */
}
.none {
  object-fit: none;
  /* The image keeps it's original size. This may result in not filling the box completely or sticking out of it. */
}
.scale-down {
  object-fit: scale-down;
  /* The result of 'none' and 'contain' is comapred and the smaller concrete object is displayed. */
}
|LiveURL=http://code.webplatform.org/gist/6badc0b20d67be7d939f
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Image Values and Replaced Content Module Level 3
|URL=http://www.w3.org/TR/css3-images/
|Status=W3C Candidate Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables={{Imported Compatibility Table}}
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=32
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
|Opera_prefixed_supported=Yes
|Opera_prefixed_version=≥ 10.6 ≤12.1, 18+
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=No
|Android_version=
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=No
|Blackberry_version=
|Blackberry_prefixed_supported=No
|Blackberry_prefixed_version=
|Chrome_mobile_supported=No
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=No
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=No
|IE_mobile_version=
|IE_mobile_prefixed_supported=No
|IE_mobile_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Yes
|Opera_mobile_prefixed_version=≥ 11 ≤12.1
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Opera
|Version=18+
|Note=The feature can be enabled through experimental web features flag from 18+
}}
}}
{{See_Also_Section
|Topic_clusters=Generated and Replaced Content, Multimedia, Video
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}