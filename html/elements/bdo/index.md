{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add Category, Parent, Children and Compatibility information. Delete HTML information sub section.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The '''bdo''' element (&lt;bdo&gt;) allows you to specify the direction in which text is to be rendered on the page. ("BDO" stands for Bi-Directional Override.)}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
|Tag_omissions=Closing tag required
|CSS_display=inline
|Content=Internationalization topics related to the <code>bdo</code> element:
* [http://www.w3.org/International/techniques/authoring-html#bdo Overriding the Unicode bidirectional algorithm]
* [http://www.w3.org/International/techniques/authoring-html#inline Mixing text direction inline]
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''BDO''' element to correct the reading order of a block of text.

The following string includes text written in the left-to-right order of the English language and the right-to-left order of Hebrew: This fragment is in English, WERBEH NI SI TNEMGARF SIHT.

Assume that the right-to-left text (WERBEH NI SI TNEMGARF SIHT.) already has been inverted, so that it displays in the correct direction. If you subsequently apply the Unicode bidirectional to the text, the text inverts a second time and incorrectly displays as left-to-right instead of right-to-left.
|Code=&lt;BDO DIR{{=}}"ltr"&gt;This fragment is in English, 
    WERBEH NI SI TNEMGARF SIHT.&lt;/BDO&gt;
|LiveURL=The solution is to override the bidirectional algorithm and put the block of text in the correct reading order inside a '''BDO''' element whose [[html/attributes/dir|'''DIR''']] attribute is set to '''ltr'''.
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
The '''BDO''' element can be used to control the reading order of a block of text.
The Unicode bidirectional algorithm automatically reverses embedded character sequences according to their inherent direction. For example, the base direction of an English document is left-to-right (ltr). If portions of a paragraph within this document contain a language with the right-to-left (rtl) reading order, you can reverse the direction of that language by applying the bidirectional algorithm.
The bidirectional algorithm and the [[html/attributes/dir|'''DIR''']] attribute generally suffice for embedded direction changes. However, incorrect presentations can occur when you expose formatted text to the bidirectional algorithm. For example, a paragraph containing English and Hebrew that is formatted for e-mail could be incorrectly inverted by the bidirectional algorithm. Because the reading order of the Hebrew text was inverted once for the e-mail, exposing it to the bidirectional algorithm would invert the words a second time.
The '''BDO''' element turns off the algorithm and controls the reading order. The [[html/attributes/dir|'''DIR''']] attribute is required when you use the '''BDO''' element.
This element is available in HTML and script as of Microsoft Internet Explorer 5.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/text-level-semantics.html#the-bdo-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/text-level-semantics.html#the-bdo-element
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/dirlang.html#edef-BDO
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections====Related pages (MSDN)===
*<code>[[css/properties/direction|direction]]</code>
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
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}