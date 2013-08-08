{{Page_Title|fragment}}
{{Flags
|Checked_Out=No
}}
{{API_Name}}
{{Summary_Section|A contiguous stretch of content.
}}
{{Concept_Page
|Content=A 'range' (or 'fragment') is a contiguous stretch of content
within a document, one that may traverse DOM nodes arbitrarily. For
example, a user may select a stretch of text that starts in the middle
of one paragraph, and ends in the middle of another. CSS styling may
apply dynamically to the
[[css/selectors/pseudo-elements/::first-line|'''::first-line''']] or
[[css/selectors/pseudo-elements/::first-letter|'''::first-letter''']]
of text.  Or a [[css/concepts/named_flow|''flow'']] of text may thread
through a series of [[css/concepts/region|''region'']] elements, each
of which may display only a portion of a paragraph that spills over
from adjacent regions within the [[css/concepts/region_chain|chain]].

You can use the [[dom/traversal/Range|DOM Range API]] to
programatically access such arbitrary stretches of content.

}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Usage=
|Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Regions Module Level 3
|URL=http://dev.w3.org/csswg/css3-regions/
|Status=W3C Editor's Draft
}}
{{See_Also_Section
|Topic_clusters=Regions
|External_links=* W3C editor's draft: [http://dev.w3.org/csswg/css3-regions/ CSS Regions Module Level 3]
* Adobe Web Standards: [http://html.adobe.com/webstandards/cssregions CSS Regions]
* Adobe Developer's Network: [http://www.adobe.com/devnet/html5/articles/css3-regions.html CSS3 Regions: Rich page layout with HTML and CSS3]
* [http://adobe.github.com/web-platform/samples/css-regions Sample pages]
}}
{{Topics|CSS-Regions}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}