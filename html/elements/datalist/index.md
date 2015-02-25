{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add Category, Parent and Children information. Complete Compatibility information.
|Checked_Out=No
|High-level issues=Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The '''datalist''' element (&lt;datalist&gt;) represents a set of [[html/elements/option|&lt;option&gt;]] elements that represent predefined options for other controls. It may be associated with an [[html/elements/input|&lt;input&gt;]] element by adding a list attribute to the input element.}}
{{Markup_Element
|DOM_interface=dom/HTMLDataListElement
|Tag_omissions=Closing tag required
|CSS_display=none
|Content=
=== Attributes ===
{{{!}} class="wikitable"
{{!}}-
!Property
{{!}}Description
{{!}}-
{{!}}[[dom/properties/options (dom/options|'''options''']]
{{!}}A collection of '''option''' objects that represent possible selections for a '''datalist''' element.
{{!}}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=
|Code=<input type="text" name="locations" list="places">
<datalist id="places">
     <option>Amman, Jordan</option>
     <option>New York, NY, USA</option>
     <option>Paris, France</option>
     <option>Vienna, Austria</option>
</datalist>
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
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/forms.html#the-datalist-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/forms.html#the-datalist-element
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Topic_clusters=HTML
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|HTML}}
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
|Chrome_version=20
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=4
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=9
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=No
|Android_version=
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=33
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=15
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=No
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=10
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}