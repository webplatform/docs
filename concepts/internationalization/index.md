{{Page_Title|Internationalization and Localization}}
{{Flags
|Checked_Out=Yes
}}
{{Summary_Section|Introduction to internationalization, best practices}}
{{Basic Page}}
==Internationalization and localization==
'''Internationalization''' (abbreviated '''i18n''', where 18 is the number of left out characters) is the design and development of a product, application or document content that enables easy localization for target audiences that vary in culture, region, or language.

'''Localization''' (abbreviated '''l10n''', where 10 is the number of left out characters) is the adaptation of a product, application or document content for a specific target audience. This includes language related aspects (translations, different characters and scripts), cultural aspects (different units, currencies, time and date formats, meaning of colors and symbols, suitability of images), and legal requirements.

Example: Internationalization is ''constructing'' a car in a way to make it possible to build in the steering wheel on either side. Localization is ''building'' cars with steering wheels on the right-hand side for a market with right-hand traffic.

Further reading: [http://www.w3.org/International/questions/qa-i18n Localization vs. Internationalization]

==Characters, fonts==
Use UTF-8 as character encoding—in each part of your system (web pages, form submission, data base). This allows you and the users of your site to use each Unicode character [http://www.w3.org/International/questions/qa-escapes#not without escaping].

Declare the character encoding in your pages using a meta element with a [[html/attributes/charset|charset attribute]] in HTML5. Because the encoding declaration must be fit within the first 1024 bytes of your HTML file it should be at the top of the head element:

<syntaxhighlight lang="html5"><!DOCTYPE html>
<html lang="…">
  <head>
    <meta charset="utf-8"/>
    <title>…</title>
    …</syntaxhighlight>

Be sure to save your documents in UTF-8. Use [http://www.w3.org/International/questions/qa-html-css-normalization normalization form NFC].

Since vintage browsers used to have problems with a leading [http://www.w3.org/International/questions/qa-byte-order-mark byte-order mark (BOM)] consider saving your files as UTF-8 without BOM. Do not use a BOM in includes because the BOM must not appear in the middle of a document.


==Language==
Declare the language of your page content with the [[html/attributes/lang|lang attribute]] on the html element. Indicate languages changes inside the document using lang attributes on elements containing the foreign phrases. For XHTML served as XML, use the xml:lang attribute. For XHTML1.x and polyglot HTML5, use both attributes with the same value.

As values, use language tags from the [http://www.iana.org/assignments/language-subtag-registry IANA Language Subtag Registry].

Language information is useful for assistive technologies like screen readers, for spell checkers etc. It is mandatory for automatic hyphenation using the CSS property [[css/properties/hyphens|hyphens]].
[http://www.w3.org/International/questions/qa-lang-why Why use the language attribute?]

Use the [[html/attributes/translate|translate attribute]] to indicate whether content and attribute values should be translated or not.

<syntaxhighlight lang="html5"><p>The national motto of France is
<i lang="fr" translate="no">Liberté, Egalité, Fraternité</i>
(freedom, equality, brotherhood).</p>
</syntaxhighlight>

Use language negotiation on multilingual Web sites. [http://www.w3.org/International/questions/qa-when-lang-neg When to use language negotiation]

Further reading: [http://www.w3.org/International/quicktips/Overview Internationalization Quick Tips for the Web]
{{Notes_Section}}
{{Topics|Internationalization}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}