{{Page_Title}}
{{Flags
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|This article looks at the different codes that can be used to represent text characters when there is a need to escape them. Included is a list containing several characters and their codes.}}
{{Markup_Structure
|Content===Common HTML entities used for typography==

=== Introduction ===
 
This article looks at the different codes that can be used to represent text characters when there is a need to escape them. There are a number of HTML entities that come in handy when there’s a need for first-rate typesetting. Many of those listed in the table below are useful only when used in foreign language copy (and copy written in specific dialects of English), so context should be taken into account before the choice is made to use them.
 
For the sake of portability, Unicode entity references should be reserved for use in documents certain to be written in the UTF-8 or UTF-16 character sets. In all other cases, the alphanumeric references should be used.

===HTML Entities Table===
{{{!}} class="wikitable"
{{!}}-
!Character(s)
!Literal(s)
!Alphanumeric value(s)
!Unicode value(s)
!Prefer to
{{!}}-
!Cent (currency)
{{!}}¢
{{!}}<code>&amp;cent;</code>
{{!}}<code>&amp;#162;</code>
{{!}}<code> </code>
{{!}}-
!Pound (currency)
{{!}}£
{{!}}<code>&amp;pound;</code>
{{!}}<code>&amp;#163;</code>
{{!}}<code> </code>
{{!}}-
!Section <sup>[[#note-sect|1]]</sup>
{{!}}§
{{!}}<code>&amp;sect;</code>
{{!}}<code>&amp;#167;</code>
{{!}}<code> </code>
{{!}}-
!Copyright
{{!}}©
{{!}}<code>&amp;copy;</code>
{{!}}<code>&amp;#169;</code>
{{!}}<code>(c)</code>
{{!}}-
!Guillemets <sup>[[#note-laquo|2]]</sup>
{{!}}« »
{{!}}<code>&amp;laquo; &amp;raquo;</code>
{{!}}<code>&amp;#171; &amp;#187;</code>
{{!}}<code>&amp;quot;</code>
{{!}}-
!Registered trademark
{{!}}®
{{!}}<code>&amp;reg;</code>
{{!}}<code>&amp;#174;</code>
{{!}}<code>(R)</code>
{{!}}-
!Degree(s)
{{!}}°
{{!}}<code>&amp;deg;</code>
{{!}}<code>&amp;#176;</code>
{{!}}<code> </code>
{{!}}-
!Plus/minus
{{!}}±
{{!}}<code>&amp;plusmn;</code>
{{!}}<code>&amp;#177;</code>
{{!}}<code>+/-</code>
{{!}}-
!Pilcrow (paragraph) <sup>[[#note-para|3]]</sup>
{{!}}¶
{{!}}<code>&amp;para;</code>
{{!}}<code>&amp;#182;</code>
{{!}}<code> </code>
{{!}}-
!Middle dot <sup>[[#note-middot|4]]</sup>
{{!}}·
{{!}}<code>&amp;middot;</code>
{{!}}<code>&amp;#183;</code>
{{!}}<code> </code>
{{!}}-
!Fractional half <sup>[[#note-frac12|5]]</sup>
{{!}}½
{{!}}<code>&amp;frac12;</code>
{{!}}<code>&amp;#188;</code>
{{!}}<code>1/2</code>
{{!}}-
!En dash <sup>[[#note-ndash|6]], [[#note-linebreak|7]]</sup>
{{!}}–
{{!}}<code>&amp;ndash;</code>
{{!}}<code>&amp;#8211;</code>
{{!}}<code>-</code> for ranges
{{!}}-
!Em (long) dash <sup>[[#note-linebreak|7]], [[#note-mdash|8]]</sup>
{{!}}—
{{!}}<code>&amp;mdash;</code>
{{!}}<code>&amp;#8212;</code>
{{!}}<code>-</code> enclosed by spaces, or <code>--</code>
{{!}}-
!Single quotes <sup>[[#note-smart_quotes|9]], [[#note-rsquo|10]]</sup>
{{!}}‘ ’
{{!}}<code>&amp;lsquo; &amp;rsquo;</code>
{{!}}<code>&amp;#8216; &amp;#8217;</code>
{{!}}<code>'</code> or <code>&amp;apos;</code>
{{!}}-
!Single low quote <sup>[[#note-low_quotes|11]]</sup>
{{!}}‚
{{!}}<code>&amp;sbquo;</code>
{{!}}<code>&amp;#8218;</code>
{{!}}<code>'</code> or comma
{{!}}-
!Double quotes <sup>[[#note-smart_quotes|9]]</sup>
{{!}}“ ”
{{!}}<code>&amp;ldquo; &amp;rdquo;</code>
{{!}}<code>&amp;#8220; &amp;#8221;</code>
{{!}}<code>", &amp;quot;</code>, <code>''</code>, or <code>``</code>
{{!}}-
!Double low quote <sup>[[#note-low_quotes|11]]</sup>
{{!}}„
{{!}}<code>&amp;bdquo;</code>
{{!}}<code>&amp;#8222;</code>
{{!}}<code>&amp;quot;</code> or <code>,,</code>
{{!}}-
!Single &amp; double daggers
{{!}}† ‡
{{!}}<code>&amp;dagger; &amp;Dagger;</code>
{{!}}<code>&amp;#8224; &amp;#8225;</code>
{{!}}<code>*</code> and <code>**</code>
{{!}}-
!Bullet
{{!}}•
{{!}}<code>&amp;bull;</code>
{{!}}<code>&amp;#8226;</code>
{{!}}<code>*</code>
{{!}}-
!Ellipsis <sup>[[#note-hellip|12]]</sup>
{{!}}…
{{!}}<code>&amp;hellip;</code>
{{!}}<code>&amp;#8230;</code>
{{!}}<code>...</code>
{{!}}-
!Prime &amp; double prime <sup>[[#note-prime|13]]</sup>
{{!}}′ ″
{{!}}<code>&amp;prime; &amp;Prime;</code>
{{!}}<code>&amp;#8242; &amp;#8243;</code>
{{!}}<code>'</code>, <code>''</code>, <code>&amp;apos;</code>, <code>&amp;quot;</code>, <code>minutes:seconds</code> elapsed
{{!}}-
!Euro sign
{{!}}€
{{!}}<code>&amp;euro;</code>
{{!}}<code>&amp;#8364;</code>
{{!}}<code> </code>
{{!}}-
!Trademark
{{!}}™
{{!}}<code>&amp;trade;</code>
{{!}}<code>&amp;#8482;</code>
{{!}}<code>(tm)</code>
{{!}}-
!Almost equal to
{{!}}≈
{{!}}<code>&amp;asymp;</code>
{{!}}<code>&amp;#8776;</code>
{{!}}<code>~</code>
{{!}}-
!Not equal to
{{!}}≠
{{!}}<code>&amp;ne;</code>
{{!}}<code>&amp;#8800;</code>
{{!}}<code>!=</code>
{{!}}-
!Less/greater than or equal to&nbsp;&nbsp;
{{!}}≤ ≥
{{!}}<code>&amp;le; &amp;ge;</code>
{{!}}<code>&amp;#8804; &amp;#8805;</code>
{{!}}<code>&lt;= or &gt;=</code>
{{!}}-
!Less/greater than
{{!}}&lt; &gt;
{{!}}<code>&amp;lt; &amp;gt;</code>
{{!}}<code>&amp;#062; &amp;#060;</code>
{{!}} 
{{!}}} 

'''Table 1:''' HTML entities useful for proper typesetting, listed in order by decimal Unicode position.

=== HTML entity usage notes ===
 
# <span id="note-sect">Citations of statute law, e.g., “29 USC § 794 (d),” are the matter most likely to reference this character.</span>
# <span id="note-laquo">Guillemets often enclose the names of stories, songs, films, public accommodations (e.g., «Rick’s Café Americain»), and popular toponyms in European languages, particularly those of the Romance sub-family. They are also used for quotes in certain European languages (such as French and Norsk); in these situations, you should always use <code>q</code> elements instead.</span>
# <span id="note-para">The pilcrow, used to mark the beginning of paragraphs that might otherwise be ambiguous, is useful when setting teaser copy. The print distribution of Rolling Stone magazine has often used such an approach. In technical writing, it might also be useful for marking an orphaned first line of a paragraph. ¶ Paragraphs marked with this symbol will most often be assigned a <code>display</code> value of <code>inline</code>, which will be explained in the introduction to the CSS layout model.</span>
# <span id="note-middot">The middle dot is an anachronistic analogue to the decimal point, still used by some designers to enumerate amounts of decimalized currency.</span>
# <span id="note-frac12">HTML also provides references to the code positions for one-quarter and three-quarters fractions.</span>
# <span id="note-ndash">The en dash is used between two quantities or dates to suggest a range, and is indistinguishable from a proper minus sign (<code>&amp;minus;</code>/<code>&amp;#8722;</code>). However, it should always be distinguished from a hyphen (<code>&amp;#45;</code>), which is used to separate the parts of an ad hoc compound word.</span>
# <span id="note-linebreak">Browsers create soft line breaks after hyphens (see above), but not after en dashes or em dashes.</span>
# <span id="note-mdash">The exclusive use of the em dash in English is to mark one or both ends of a dependent clause in lieu of parentheses, and to indicate that if spoken aloud the clause should be preceded and followed by uninflected pauses. In several other languages&mdash;particularly those of the Slavic sub-family&mdash;em dashes indicate dialogue from the beginning of a paragraph. Tradition dictates that this character not be enclosed itself by spaces, but the thoughtful user of markup may wish to do just that in order to avoid an especially ragged line.</span>
# <span id="note-smart_quotes">These are the members of the automated “Smart Quotes” set of characters incorporated into most popular word processing platforms.  They are often encoded at vendor-specific code positions rather than Unicode or ISO Latin code positions, which can cause problems when they are copied into a Web document.</span>
# <span id="note-rsquo">The single close quote character is also used in English as the apostrophe.</span>
# <span id="note-low_quotes">Low quotes are used in several Central and Eastern European langauges in preference to the analogous English opening and closing quote characters.</span>
# <span id="note-hellip">Since the ellipsis is a single character, the tracking of its constituent glyphs will ''not'' be affected by any value set for the <code>letter-spacing</code> or <code>text-align</code> properties.</span>
# <span id="note-prime">Primes are used to denote minutes (of both time elapsed and arc) and feet as units of measurement; the double prime in its turn denotes seconds and inches. The use of these characters in relation to units of time elapsed has decreased in popularity in recent years, a decrease that correlates strongly with the increased availability of word processing systems (and their common use by non-specialist operators). Many fonts use prime and double prime characters indistinguishable from single and double close quotes, but for reasons of portability these entities should still be used when called for, notwithstanding the characteristics of the intended display face.</span>
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
|Not_required=Yes
|Imported_tables=
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