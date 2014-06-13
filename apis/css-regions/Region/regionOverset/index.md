{{Page_Title|regionOverset}}
{{Flags
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|A [[css/concepts/region|region's]] display state within a [[css/concepts/region_chain|region chain]].}}
{{API_Object_Property
|Property_applies_to=apis/css-regions/Region
|Read_only=Yes
|Example_object_name=region
|Return_value_name=regionState
|Javascript_data_type=String
|Return_value_description=A [[css/concepts/region|region's]] display state within a [[css/concepts/region_chain|region chain]]:

* '''overset''' indicates the region is the last in the [[css/concepts/region_chain|chain]], and does not have enough room to display remaining content. See [[css/properties/region-fragment|'''region-fragment''']] for display options.

* '''empty''' indicates content was accommodated by previous regions in the [[css/concepts/region_chain|chain]], or that no content is available to flow into the [[css/concepts/region_chain|chain]].

* '''fit''' indicates various scenarios:

** When content appears within the last region in the [[css/concepts/region_chain|chain]] but does not overflow it, as described above in '''overset'''

** For regions that flow content into subsequent regions in the [[css/concepts/region_chain|chain]]

** For regions that are too small to display the next available item of content, such as an image, which gets pushed into a subsequent region

** For elements that no longer behave as a region, which occurs when their [[css/properties/flow-from|'''flow-from''']] property reverts to '''none'''
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Check if region needs to be deleted or appended:
|Code=if (region.regionOverset == 'empty') {
    // delete region?
} else if (region.regionOverset == 'overset') {
    // add additional regions?
}
}}
}}
{{Notes_Section
|Notes=Not to be confused with [[apis/css-regions/NamedFlow/overset|'''overset''']], which indicates whether the overall [[css/concepts/named_flow|named flow]] features too few display regions.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Regions Module Level 3
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
|Topic_clusters=Regions
|External_links=* W3C editor's draft: [http://dev.w3.org/csswg/css3-regions/ CSS Regions Module Level 3]
* Adobe Web Standards: [http://html.adobe.com/webstandards/cssregions CSS Regions]
* Adobe Developer's Network: [http://www.adobe.com/devnet/html5/articles/css3-regions.html CSS3 Regions: Rich page layout with HTML and CSS3]
* [http://adobe.github.com/web-platform/samples/css-regions Sample pages]
}}
{{Topics|API, CSS, CSS-Regions}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}