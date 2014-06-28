{{Page_Title|content fragments}}
{{Flags
|State=Almost Ready
|Editorial notes=Fix or remove broken link to DOM API; 
|Checked_Out=No
}}
{{API_Name}}
{{Summary_Section|A contiguous range of content, which may stretch arbitrarily across DOM nodes.}}
{{Concept_Page
|Content=A ''range'' (or ''fragment'') is a contiguous stretch of content within a document, one that may traverse DOM nodes arbitrarily. For example, a user may select a stretch of text that starts in the middle of one paragraph, and ends in the middle of another. CSS styling may apply dynamically to the [[css/selectors/pseudo-elements/&#58;&#58;first-line|'''&#58;&#58;first-line''']] or [[css/selectors/pseudo-elements/&#58;&#58;first-letter|'''&#58;&#58;first-letter''']] of text.  Or a [[css/concepts/named_flow|''flow'']] of text may thread through a series of [[css/concepts/region|''region'']] elements, each of which may display only a portion of a paragraph that spills over from adjacent regions within the [[css/concepts/region_chain|chain]].

You can use the [[dom/traversal/Range|DOM Range API]] to programatically access such arbitrary stretches of content.
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Topic_clusters=Regions
}}
{{Topics|CSS-Regions}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}