{{Page_Title|flow-into}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Diverts the selected element's content into a [[css/concepts/named_flow|named flow]], used to thread content through different layout [[css/concepts/region|regions]] specified by  [[css/properties/flow-from|'''flow-from''']].}}
{{CSS Property
|Initial value=none
|Applies to=Any element. The flow-into property does not apply to any pseudo-element such as first-line, first-letter, before or after.
|Inherited=No
|Media=visual
|Computed value=as specified
|Animatable=No
|CSS object model property=flowInto
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=<ident>
|Description=Identifier that specifies a named flow into which to place element's content.
}}{{CSS Property Value
|Data Type=none
|Description=The element's content remains unchanged, and is not diverted to a flow unless an ancestor element specifies it.
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
|Description=...flows the article through the series of '''div''' elements, transforming them into [[css/concepts/region|''regions'']] and replacing the placeholder text:
|Code=<!-- CONTENT -->

<article class="content">
  ...
</article>

<!-- LAYOUT -->

<section class="layout">
  <div>Region #1</div>
  <div>Region #2</div>
  <div>Region #3</div>
  <div>Region #4</div>
  <div>Region #5</div>
</section>
}}
}}
{{Notes_Section
|Usage=The [[css/properties/flow-into|'''flow-into''']] property diverts content from where it would ordinarily appear in the document to a 'named flow'.  It reappears elsewhere flowing through a series of [[css/concepts/region|''region'']] elements whose [[css/properties/flow-from|'''flow-from''']] specifies the same named flow.

An element whose [[css/properties/flow-into|'''flow-into''']] specifies a named flow takes its descendents along with it by default, with two exceptions:

* If a descendent specifies a different named flow, it can be presented in a different series of regions specified by a corresponding [[css/properties/flow-from|'''flow-from''']].

* If a descendent specifies the same named flow, it is moved from within the content and then appended.

Setting a descendent's [[css/properties/flow-into|'''flow-into''']] to '''none''' has no effect, and cannot be used to prevent the descendent from flowing along with the ancestor.

More than one element can contribute to the same named flow, in which case their DOM order determines how they appear output within regions.

For an overview of CSS Regions, see [[tutorials/css-regions|Using CSS Regions to flow content through a layout]].
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Regions Module Level 3
|URL=http://dev.w3.org/csswg/css3-regions/
|Status=Editor's Draft
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
* [http://codepen.io/collection/jabto Additional examples on codpen.io]. This experimental feature is in WebKit (Chrome and Safari) and Trident (Internet Explorer). Enable experimental features to see how CSS Regions works.
}}
{{Topics|CSS, CSS-Regions}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}