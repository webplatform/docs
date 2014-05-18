{{Page_Title|abbr}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Use the '''abbr''' element to indicate an abbreviation or acronym.}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
|Content=The '''abbr''' is a phrasing-level element used to indicate an abbreviation or acronym. It can’t contain block-level elements, but it can contain other phrasing type elements.

The '''abbr''' element’s role has been expanded to incorporate the role previously performed by [[html/acronym|'''acronym''' element]] (which has been deprecated).

==Attributes==

A '''abbr''' element may optionally have a [[html/attributes/title|'''title''' attribute]] that must contain an expansion of the abbreviation (and nothing else). The '''abbr''' element can accept any attributes permitted globally (e.g. '''class''').
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following example shows how to use the '''abbr''' element with an optional [[html/attributes/title|'''title''']] attribute.
|Code=<syntaxhighlight lang="html5">
<p>The national capital of the United States is located in Washington, <abbr title="District of Columbia">D.C.</abbr>.</p>
</syntaxhighlight>
|LiveURL=http://code.webplatform.org/gist/939206
}}
}}
{{Notes_Section
|Usage=Abbreviations don’t have to marked up in the '''abbr''' element, but it can be useful

* When you want to provide an expanded version of the term;
* When you are using a term that may be unfamiliar to your audience; or
* When you want to visually-separate abbreviations from other content on the page (using CSS).

In the first two instances, it would make sense to include an expansion of the abbreviation in a '''title''' attribute.
|Notes=If you use the same abbreviation multiple times in a  document, you might consider using a '''title''' to expand the first instance (perhaps wrapping it in a [[html/dfn|'''dfn''' element] to mark it as the defining instance) and then leave the '''title''' attribute off of the additional instances. This may provide a better reading experience for assistive technologies, but it should be noted that the instances without '''title''' attributes will not provide the expanded text as each '''abbr''' is independent (expansions are not shared among identical '''abbr'' elements).
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 4.01 Specification
|URL=http://www.w3.org/TR/html401/struct/text.html#edef-ABBR
|Status=W3C Recommendation
}}{{Related Specification
|Name=HTML 5.x
|URL=http://www.w3.org/html/wg/drafts/html/master/text-level-semantics.html#the-abbr-element
|Status=W3C Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=22.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=16.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=8.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=HTML, Text
}}
{{Topics|HTML, XHTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/HTML/Element/abbr
|MSDN_link=
|HTML5Rocks_link=
}}