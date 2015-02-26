{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Used to provide fallback text to be shown by user agents that don't support ruby annotations}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
|Tag_omissions=Closing tag omissible in certain cases
|CSS_display=none
|Content=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The example above, in which each ideograph in the text 漢字 is annotated with its phonetic reading, could be expanded to use rp so that in legacy user agents the readings are in parentheses
|Code=<nowiki>
<p lang="ja" xml:lang="ja">
...
<ruby>
 漢 <rp>(</rp><rt>かん</rt><rp>)</rp>
 字 <rp>(</rp><rt>じ</rt><rp>)</rp>
</ruby>
...
</p>
</nowiki>
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
|URL=http://www.w3.org/TR/html51/text-level-semantics.html#the-rp-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/text-level-semantics.html#the-rp-element
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}