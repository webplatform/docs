{{Page_Title|flow-from property}}
{{Flags}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Flows content from a named flow (specified by a corresponding [[css/properties/flow-into|'''flow-into''']]) through selected elements to form a dynamic chain of layout ''regions''.}}
{{CSS Property
|Initial value=none
|Inherited=No
|Media=visual
|Animatable=No
|CSS object model property=flowFrom
|Values={{CSS Property Value
|Data Type=identifier
|Description=Replaces content from specified named flow, flowing it from one ''region'' element to another.
}}{{CSS Property Value
|Data Type=none
|Description=Keeps element as is, and does not transform it into a region and replace its content.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The following CSS...
|Code=article.content {
    flow-into: main;
}

section.layout > div {
    flow-from: main;
}
}}{{Single Example
|Language=HTML
|Description=...flows the article through the series of '''div''' elements, transforming them into ''regions'' and replacing the placeholder text:
|Code=&amp;lt;!-- CONTENT -->

&amp;lt;article class="content">
  ...
&amp;lt;/article>

&amp;lt;!-- LAYOUT -->

&amp;lt;section class="layout">
  &amp;lt;div>Region #1&amp;lt;/div>
  &amp;lt;div>Region #2&amp;lt;/div>
  &amp;lt;div>Region #3&amp;lt;/div>
  &amp;lt;div>Region #4&amp;lt;/div>
  &amp;lt;div>Region #5&amp;lt;/div>
&amp;lt;/section>
}}
}}
{{Notes_Section
|Usage=While regions can be positioned arbitrarily on the screen, their order in the document determines the order in which content flows. Regions otherwise do not have to appear as a continuous series within the DOM.

Descendants of any element whose [[css/properties/flow-from|'''flow-from''']] specifies a named flow are suppressed from display, making their own [[css/properties/flow-from|'''flow-from''']] values irrelevant.

For an overview of CSS Regions, see [[tutorials/css-regions|Using CSS Regions to flow content through a layout]].
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Regions Module Level 3
|URL=http://dev.w3.org/csswg/css3-regions/
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=No
|Chrome_version=
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=20
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=No
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Yes
|Internet_explorer_prefixed_version=8
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=Yes
|Safari_prefixed_version=534
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
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
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
|Browser=Internet Explorer
|Version=8
|Note=Supports only [[css/properties/flow-into|'''flow-into''']] and [[css/properties/flow-from|'''flow-from''']] properties in Compatibility Mode 5.
}}{{Compatibility Notes Row
|Browser=Internet Explorer
|Version=10
|Note=Supports only [[css/properties/flow-into|'''flow-into''']] and [[css/properties/flow-from|'''flow-from''']] properties in Compatibility Mode 9.
}}
}}
{{See_Also_Section
|Topic_clusters=Regions
|External_links=* W3C editor's draft: [http://dev.w3.org/csswg/css3-regions/ CSS Regions Module Level 3]
* Adobe Web Standards: [http://html.adobe.com/webstandards/cssregions CSS Regions]
* Adobe Developer's Network: [http://www.adobe.com/devnet/html5/articles/css3-regions.html CSS3 Regions: Rich page layout with HTML and CSS3]
* [http://adobe.github.com/web-platform/samples/css-regions Sample pages]
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}