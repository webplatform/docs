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
<p>The national capital of the 
United States is located in Washington, 
<abbr title="District of Columbia">D.C.</abbr>.</p>
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
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}