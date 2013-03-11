{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|One or more tokens that define the matching criteria for the distribution of child nodes of the shadow host.}}
{{Markup_Attribute
|Applies_to=dom/HTMLContentElement
|Property_applies_to=html/elements/content
|Content=The select tokens define the matching criteria for distributing child nodes of the shadow host. Each token must be a valid selector fragment, which consists of the following:
* a selector that uniquely identifies the shadow host.
* a combination selector that identifies the parent element and the element at this insertion point.
* the following [http://www.w3.org/TR/css3-selectors CSS3 selector types]:
** [http://www.w3.org/TR/css3-selectors/#type-selectors type selector].
** [http://www.w3.org/TR/css3-selectors/#universal-selector universal selector].
** [http://www.w3.org/TR/css3-selectors/#class-html class selector].
** [http://www.w3.org/TR/css3-selectors/#id-selectors ID selector].
** [http://www.w3.org/TR/css3-selectors/#attribute-selectors attribute selector].
** The following pseudo-class selectors: 
*** link
*** visited
*** target
*** enabled
*** disabled
*** checked
*** indeterminate
*** nth-child()
*** nth-last-child()
*** nth-of-type()
*** nth-last-of-type()
*** first-child
*** last-child
*** first-of-type
*** last-of-type
*** only-of-type
}}
{{Examples_Section
|Not_required=No
|Examples=
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
|Chrome_version=26
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Unknown
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Web Components
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}