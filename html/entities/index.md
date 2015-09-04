---
title: entities
tags:
  - Markup
  - Structures
  - HTML
readiness: 'Ready to Use'
summary: 'This article looks at the different codes that can be used to represent text characters when there is a need to escape them. Included is a list containing several characters and their codes.'
uri: html/entities

---
# entities

## Summary

This article looks at the different codes that can be used to represent text characters when there is a need to escape them. Included is a list containing several characters and their codes.

## Common HTML entities used for typography

### Introduction

This article looks at the different codes that can be used to represent text characters when there is a need to escape them. There are a number of HTML entities that come in handy when there’s a need for first-rate typesetting. Many of those listed in the table below are useful only when used in foreign language copy (and copy written in specific dialects of English), so context should be taken into account before the choice is made to use them.

For the sake of portability, Unicode entity references should be reserved for use in documents certain to be written in the UTF-8 or UTF-16 character sets. In all other cases, the alphanumeric references should be used.

### HTML Entities Table

Character(s)
:   Literal(s)
Cent (currency)
:   ¢
Pound (currency)
:   £
Section <sup>[1](#note-sect)</sup>
:   §
Copyright
:   ©
Guillemets <sup>[2](#note-laquo)</sup>
:   « »
Registered trademark
:   ®
Degree(s)
:   °
Plus/minus
:   ±
Pilcrow (paragraph) <sup>[3](#note-para)</sup>
:   ¶
Middle dot <sup>[4](#note-middot)</sup>
:   ·
Fractional half <sup>[5](#note-frac12)</sup>
:   ½
En dash <sup>[6](#note-ndash),\\ [7](#note-linebreak)</sup>
:   –
Em (long) dash <sup>[7](#note-linebreak),\\ [8](#note-mdash)</sup>
:   —
Single quotes <sup>[9](#note-smart_quotes),\\ [10](#note-rsquo)</sup>
:   ‘ ’
Single low quote <sup>[11](#note-low_quotes)</sup>
:   ‚
Double quotes <sup>[9](#note-smart_quotes)</sup>
:   “ ”
Double low quote <sup>[11](#note-low_quotes)</sup>
:   „
Single & double daggers
:   † ‡
Bullet
:   •
Ellipsis <sup>[12](#note-hellip)</sup>
:   …
Prime & double prime <sup>[13](#note-prime)</sup>
:   ′ ″
Euro sign
:   €
Trademark
:   ™
Almost equal to
:   ≈
Not equal to
:   �
Less/greater than or equal to �
:   ≤ ≥
Less/greater than
:   \< \>

**Table 1:** HTML entities useful for proper typesetting, listed in order by decimal Unicode position.

### HTML entity usage notes

1.  <span id="note-sect">Citations of statute law, e.g., “29 USC § 794 (d),” are the matter most likely to reference this character.</span>
2.  <span id="note-laquo">Guillemets often enclose the names of stories, songs, films, public accommodations (e.g., «Rick’s Café Americain»), and popular toponyms in European languages, particularly those of the Romance sub-family. They are also used for quotes in certain European languages (such as French and Norsk); in these situations, you should always use `q` elements instead.</span>
3.  <span id="note-para">The pilcrow, used to mark the beginning of paragraphs that might otherwise be ambiguous, is useful when setting teaser copy. The print distribution of Rolling Stone magazine has often used such an approach. In technical writing, it might also be useful for marking an orphaned first line of a paragraph. ¶ Paragraphs marked with this symbol will most often be assigned a `display` value of `inline`, which will be explained in the introduction to the CSS layout model.</span>
4.  <span id="note-middot">The middle dot is an anachronistic analogue to the decimal point, still used by some designers to enumerate amounts of decimalized currency.</span>
5.  <span id="note-frac12">HTML also provides references to the code positions for one-quarter and three-quarters fractions.</span>
6.  <span id="note-ndash">The en dash is used between two quantities or dates to suggest a range, and is indistinguishable from a proper minus sign (`&minus;`/`&#8722;`). However, it should always be distinguished from a hyphen (`&#45;`), which is used to separate the parts of an ad hoc compound word.</span>
7.  <span id="note-linebreak">Browsers create soft line breaks after hyphens (see above), but not after en dashes or em dashes.</span>
8.  <span id="note-mdash">The exclusive use of the em dash in English is to mark one or both ends of a dependent clause in lieu of parentheses, and to indicate that if spoken aloud the clause should be preceded and followed by uninflected pauses. In several other languages—particularly those of the Slavic sub-family—em dashes indicate dialogue from the beginning of a paragraph. Tradition dictates that this character not be enclosed itself by spaces, but the thoughtful user of markup may wish to do just that in order to avoid an especially ragged line.</span>
9.  <span id="note-smart_quotes">These are the members of the automated “Smart Quotes” set of characters incorporated into most popular word processing platforms. They are often encoded at vendor-specific code positions rather than Unicode or ISO Latin code positions, which can cause problems when they are copied into a Web document.</span>
10. <span id="note-rsquo">The single close quote character is also used in English as the apostrophe.</span>
11. <span id="note-low_quotes">Low quotes are used in several Central and Eastern European langauges in preference to the analogous English opening and closing quote characters.</span>
12. <span id="note-hellip">Since the ellipsis is a single character, the tracking of its constituent glyphs will *not* be affected by any value set for the `letter-spacing` or `text-align` properties.</span>
13. <span id="note-prime">Primes are used to denote minutes (of both time elapsed and arc) and feet as units of measurement; the double prime in its turn denotes seconds and inches. The use of these characters in relation to units of time elapsed has decreased in popularity in recent years, a decrease that correlates strongly with the increased availability of word processing systems (and their common use by non-specialist operators). Many fonts use prime and double prime characters indistinguishable from single and double close quotes, but for reasons of portability these entities should still be used when called for, notwithstanding the characteristics of the intended display face.</span>

