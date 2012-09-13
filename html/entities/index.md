{{Flags
|High-level issues=Stub
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Markup_Structure
|Content===Common HTML entities used for typography==
Stub.


Pre-table text.

{{{!}} class="wikitable"
{{!}}-
! Header text
! Header text
! Header text
{{!}}-
{{!}} Example ¢
{{!}} Example &amp;cent;
{{!}} Example &amp;#162;
{{!}}}

Post-table text.

== Introduction ==
 
This article looks at the different codes that can be used to represent text characters when there is a need to escape them. There are a number of HTML entities that come in handy when there’s a need for first-rate typesetting. Many of those listed in Table 1 below are useful only when used in foreign language copy (and copy written in specific dialects of English), so context should be taken into account before the choice is made to use them.
 
For the sake of portability, Unicode entity references should be reserved for use in documents certain to be written in the UTF-8 or UTF-16 character sets. In all other cases, the alphanumeric references should be used.


'''Table 1:''' HTML entities useful for proper typesetting, listed in order by decimal Unicode position.

=== HTML entity usage notes ===
 
# Citations of statute law, eg, “29 USC § 794 (d),” are the matter most likely to reference this character.
# Guillemets often enclose the names of stories, songs, films, public accommodations (eg, «Rick’s Café Americain»), and popular toponyms in European languages, particularly those of the Romance sub-family. They are also used for quotes in certain European languages (such as French and Norsk); in these situations, you should always use <code>q</code> elements instead.
# The pilcrow, used to mark the beginning of paragraphs that might otherwise be ambiguous, is useful when setting teaser copy. The print distribution of Rolling Stone magazine has often used such an approach. In technical writing, it might also be useful for marking an orphaned first line of a paragraph. ¶ Paragraphs marked with this symbol will most often be assigned a <code>display</code> value of <code>inline</code>, which will be explained in the introduction to the CSS layout model.
# The middle dot is an anachronistic analogue to the decimal point, still used by some designers to enumerate amounts of decimalized currency.
# HTML also provides references to the code positions for one-quarter and three-quarters fractions.
# The en dash is used between two quantities or dates to suggest a range, and is indistinguishable from a proper minus sign (<code>&amp;minus;</code>/<code>&amp;#8722;</code>). However, it should always be distinguished from a hyphen (<code>&amp;#45;</code>), which is used to separate the parts of an ad hoc compound word.
# Browsers create soft linebreaks after hyphens (see above), but not after en dashes or em dashes.
# The exclusive use of the em dash in English is to mark one or both ends of a dependent clause in lieu of parentheses, and to indicate that if spoken aloud the clause should be preceded and followed by uninflected pauses.  In several other languages — particularly those of the Slavic sub-family — em dashes indicate dialogue from the beginning of a paragraph. Tradition dictates that this character not be enclosed itself by spaces, but the thoughtful user of markup may wish to do just that in order to avoid an especially ragged line.
# These are the members of the automated “Smart Quotes” set of characters incorporated into most popular word processing platforms.  They are often encoded at vendor-specific code positions rather than Unicode or ISO Latin code positions, which can cause problems when they are copied into a Web document.
# The single close quote character is also used in English as the apostrophe.
# Low quotes are used in several Central and Eastern European langauges in preference to the analogous English opening quote characters.
# Since the ellipsis is a single character, the tracking of its constituent glyphs will ''not'' be affected by any value set for the <code>letter-spacing</code> or <code>text-align</code> properties.
# Primes are used to denote minutes (of both time elapsed and arc) and feet as units of measurement; the double prime in its turn denotes seconds and inches.  The use of these characters in relation to units of time elapsed has decreased in popularity in recent years, a decrease that correlates strongly with the increased availability of word processing systems (and their common use by non-specialist operators). Many fonts use prime and double prime characters indistinguishable from single and double close quotes, but for reasons of portability these entities should still be used when called for, notwithstanding the characteristics of the intended display face.
 
''Note:'' This material was originally published as part of the Opera Web Standards Curriculum, available as [http://dev.opera.com/articles/view/supplementary-common-html-entities-used/ Supplementary: Common HTML entities used for typography], written by Ben Henick. Like the original, it is published under the [http://creativecommons.org/licenses/by-nc-sa/2.5/ Creative Commons Attribution, Non Commercial - Share Alike 2.5] license.


}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}
}