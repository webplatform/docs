{{Page_Title|region-fragment}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Controls whether the last [[css/concepts/region|''region'']] in a [[css/concepts/region_chain|chain]] displays additional 'overset' content according its default [[css/properties/overflow|'''overflow''']] property, or	if it displays a [[css/concepts/fragment|fragment]] of content as if it were flowing into a subsequent region.}}
{{CSS Property
|Initial value=auto
|Applies to=CSS Regions
|Inherited=No
|Media=visual
|Computed value=specified value
|Animatable=No
|CSS object model property=regionFragment
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=auto
|Description=Region element displays [[css/concepts/overset|overset]] content according to its [[css/properties/overflow|'''overflow''']] property.
}}{{CSS Property Value
|Data Type=break
|Description=Region element overrides [[css/properties/overflow|'''overflow''']] property, displaying whatever fragment of [[css/concepts/overset|overset]] content can fit within the region.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=<style>
  article {
    flow-into: article-flow;
  }
  #region-1, #region-2 {
    flow-from: article-flow;
    region-fragment: break; /* or auto */
    overflow: visible; /* or hidden */
  }
</style>

<body>
  <article>...</article>
  <div id="region-1"></div>
  <div id="region-2"></div>
</body>
}}
}}
{{Notes_Section
|Usage=In the following example, 'region_1' can accommodate the article's gray text, 'region_2' can	accommodate the blue text, and the red	'overset' text does not fit within the [[css/concepts/region_chain|region chain]]:

[[Image:region_fragment.png]]

Setting '''region-fragment''' to '''break''' suppresses display of the [[css/concepts/overset|overset]] text, as shown in the example at the bottom.  Setting '''region-fragment''' to its default '''auto''' value makes overset content display according to whatever [[css/properties/overflow|'''overflow''']] property is defined, as shown in the two examples on the right. Even '''overflow:hidden''' may display part of the first line of overset text.

The property only applies to the final element in a [[css/concepts/region_chain|''region chain'']] that is not large enough to accomodate remaining content. To behave as a 'region', the element's [[css/properties/flow-from|'''flow-from''']] must specify a [[css/concepts/named_flow|named flow]], and display content from a corresponding [[css/properties/flow-into|'''flow-into''']].

For an overview of CSS Regions, see [[tutorials/css-regions|Using CSS Regions to flow content through a layout]].
|Notes=This property was formerly named '''region-overflow'''.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Regions Module Level 1
|URL=http://www.w3.org/TR/css3-regions/
|Status=W3C Working Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=No
|Chrome_version=
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
|Safari_mobile_prefixed_supported=Yes
|Safari_mobile_prefixed_version=537
}}
|Notes_rows=
}}
{{See_Also_Section
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