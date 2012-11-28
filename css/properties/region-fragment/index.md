{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Controls whether the last ''region'' in a chain displays additional
''overset'' content according its default
[[css/properties/overflow|'''overflow''']] property, or	if it displays
a fragment of content as if it were flowing into a subsequent region.
}}
{{CSS Property
|Initial value=auto
|Applies to=CSS Regions
|Inherited=Yes
|Media=visual
|Computed value=specified value
|Animatable=No
|CSS object model property=regionFragment
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=auto
|Description=Region element displays overset content according to its [[css/properties/overflow|'''overflow''']] property.
}}{{CSS Property Value
|Data Type=break
|Description=Region element overrides [[css/properties/overflow|'''overflow''']] property, displaying whatever fragment of overset content can fit within the region.
}}
}}
{{Examples_Section
|Not_required=Yes
|Examples={{Single Example}}
}}
{{Notes_Section
|Usage=In the following example, ''region_1'' can accommodate the article's gray text, ''region_2'' can	accommodate the blue text, and the red	''overset'' text can't fit within the region chain:

[[Image:region_fragment.png]]

Setting '''region-fragment''' to '''break''' suppresses display of the overset text, as shown in the example at the bottom.  Setting '''region-fragment''' to its default '''auto''' value makes overset content display according to whatever [[css/properties/overflow|'''overflow''']] property is defined, as shown in the two examples on the right. Even '''overflow:hidden''' may display part of the first line of overset text.

The property only applies to the final element in a ''region chain'' that is not large enough to accomodate remaining content. To behave as a ''region'', the element's [[css/properties/flow-from|'''flow-from''']] must specify a named flow, and display content from a corresponding [[css/properties/flow-into|'''flow-into''']].

See [[tutorials/css-regions|Using CSS Regions to flow content through a layout]] for an overview of CSS Regions.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Regions Module Level 3
|URL=http://dev.w3.org/csswg/css3-regions/#the-region-fragment-property
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
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Regions
|Manual_links=* [[tutorials/css-regions|Using CSS Regions to flow content through a layout]]
|External_links=* [http://html.adobe.com/webstandards/cssregions Adobe Web Standards: CSS Regions]
* [http://www.adobe.com/devnet/html5/articles/css3-regions.html CSS3 regions: Rich page layout with HTML and CSS3]
* [http://adobe.github.com/web-platform/samples/css-regions Sample pages]
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}