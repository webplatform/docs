{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Events section must be modified.
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Groups inline elements in a document. The span element is both style and semantics '''neutral'''; it does not assign any style attributes or semantic meaning on its own.}}
{{Markup_Element
|DOM_interface=dom/HTMLSpanElement
|Tag_omissions=Closing tag required
|CSS_display=inline
|Content=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''span''' element to create an inline text container that changes the color of a word to blue.
|Code=&lt;p&gt;This paragraph contains a single &lt;span style{{=}}"color: blue"&gt;blue&lt;/span&gt; word.
|LiveURL=
}}{{Single Example
|Language=HTML
|Description=This example uses the '''span''' element to add a simple [http://microformats.org/wiki/microformats2#h-card Microformats2 h-card] to a person's name.
|Code=&lt;span class{{=}}"h-card vcard"&gt;Pius Uzamere&lt;/span&gt;
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
The '''SPAN''' element is especially useful for applying cascading style sheets (CSS) styles.

=== History ===

The span element was not initially part of HTML. 

On July 3, 1995, Benjamin C. W. Sittler [http://lists.w3.org/Archives/Public/www-style/1995Jul/0003.html proposes] a '''generic text container tag''' [[HTML/Elements/text|<text>]] for applying styles to certain blocks of text. The rendering is neutral except if used in conjunction of a stylesheet. There is a [http://lists.w3.org/Archives/Public/www-style/1995Jul/thread.html#msg11 debate] around [[HTML/Elements/c|<c>]] versus [[HTML/Elements/text|<text>]] about readability, meaning. Bert Bos is [http://lists.w3.org/Archives/Public/www-style/1995Jul/0016.html mentioning] the extensibility nature of the [[HTML/Elements/text|<text>]]  element through the [[Attributes/class|class]] attribute (with values such as city, person, date, etc.). Paul Prescod is [http://lists.w3.org/Archives/Public/www-style/1995Jul/0017.html worried] that both elements will be abused. He is opposed to text mentionning that ''"any new element should be on an old one"'' and adding ''"If we create a tag with no semantics it can be used anywehere without ever being wrong.  We must force authors to properly tag the semantics of their document.  We must force editor vendors to make that choice explicit in their interfaces."''

&lt;span&gt; has been introduced to html through the internationalization WG on September 25, 1995 in the [http://tools.ietf.org/html/draft-ietf-html-i18n-01 second draft html-i18n]. The purpose was to create a generic container needed to carry the [[Attributes/lang|lang]] and [[Attributes/bidi|bidi]] attributes in cases where no other element is appropriate. 

The [http://tools.ietf.org/html/draft-ietf-html-style-00 first draft of html-style] had the [[HTML/Elements/c|<c>]] element in its table of content with the purpose of applying a style to some text which doesn't have a structural role. Michael J Hannah on  December 5, 1995 [http://lists.w3.org/Archives/Public/www-style/1995Dec/0039.html proposes] to get rid of the new HTML element [[HTML/Elements/c|<c>]] to use the new element <span> part of the internationalization proposal [http://tools.ietf.org/html/draft-ietf-html-i18n-01 draft-ietf-html-i18n] because it will be able to carry the [[Attributes/style|style]] attribute. Then in the 23 January 1996 version of the [http://tools.ietf.org/html/draft-ietf-html-style-01 html-style] it has been replaced by the &lt;span&gt; element.

But we had to wait until [http://www.w3.org/TR/html401/ HTML 4.01] to see the new element be [http://www.w3.org/TR/html401/struct/global.html#edef-SPAN part of the HTML] language. It appears on the HTML 4 W3C Working Draft on September 17, 1997.

|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/text-level-semantics.html#the-span-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/text-level-semantics.html#the-span-element
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/global.html#edef-SPAN
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
|Chrome_version=All versions
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=All versions
|Firefox_supported=Yes
|Firefox_version=All versions
|Firefox_prefixed_supported=Yes
|Firefox_prefixed_version=All versions
|Internet_explorer_supported=Yes
|Internet_explorer_version=All versions
|Internet_explorer_prefixed_supported=Yes
|Internet_explorer_prefixed_version=All versions
|Opera_supported=Yes
|Opera_version=All versions
|Opera_prefixed_supported=Yes
|Opera_prefixed_version=All versions
|Safari_supported=Yes
|Safari_version=All versions
|Safari_prefixed_supported=Yes
|Safari_prefixed_version=All versions
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=All versions
|Android_prefixed_supported=Yes
|Android_prefixed_version=All versions
|Blackberry_supported=Yes
|Blackberry_version=All versions
|Blackberry_prefixed_supported=Yes
|Blackberry_prefixed_version=All versions
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=All versions
|Chrome_mobile_prefixed_supported=Yes
|Chrome_mobile_prefixed_version=All versions
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=All versions
|Firefox_mobile_prefixed_supported=Yes
|Firefox_mobile_prefixed_version=All versions
|IE_mobile_supported=Yes
|IE_mobile_version=All versions
|IE_mobile_prefixed_supported=Yes
|IE_mobile_prefixed_version=All versions
|Opera_mobile_supported=Yes
|Opera_mobile_version=All versions
|Opera_mobile_prefixed_supported=Yes
|Opera_mobile_prefixed_version=All versions
|Opera_mini_supported=Yes
|Opera_mini_version=All versions
|Opera_mini_prefixed_supported=Yes
|Opera_mini_prefixed_version=All versions
|Safari_mobile_supported=Yes
|Safari_mobile_version=All versions
|Safari_mobile_prefixed_supported=Yes
|Safari_mobile_prefixed_version=All versions
}}
|Notes_rows=
}}