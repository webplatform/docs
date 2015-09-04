---
title: internationalization
tags:
  - Basic
  - Pages
  - Internationalization
readiness: 'Ready to Use'
summary: 'Introduction to internationalization, best practices'
uri: concepts/internationalization

---
# Internationalization and Localization

## Summary

Introduction to internationalization, best practices

## Internationalization and localization

**Internationalization** (abbreviated **i18n**, where 18 is the number of left out characters) is the design and development of a product, application or document content that enables easy localization for target audiences that vary in culture, region, or language.

**Localization** (abbreviated **l10n**, where 10 is the number of left out characters) is the adaptation of a product, application or document content for a specific target audience. This includes language related aspects (translations, different characters and scripts), cultural aspects (different units, currencies, time and date formats, meaning of colors and symbols, suitability of images), and legal requirements.

Example: Internationalization is *constructing* a car in a way to make it possible to build in the steering wheel on either side. Localization is *building* cars with steering wheels on the right-hand side for a market with right-hand traffic.

Further reading: [Localization vs. Internationalization](http://www.w3.org/International/questions/qa-i18n)

## Characters, fonts

Use UTF-8 as character encoding—in each part of your system (web pages, form submission, data base). This allows you and the users of your site to use each Unicode character [without escaping](http://www.w3.org/International/questions/qa-escapes#not).

Declare the character encoding in your pages using a meta element with a [charset attribute](/html/attributes/charset) in HTML5. Because the encoding declaration must be fit within the first 1024 bytes of your HTML file it should be at the top of the head element:

``` {.html}
<!DOCTYPE html>
<html lang="…">
  <head>
    <meta charset="utf-8"/>
    <title>…</title>
    …
```

 Be sure to save your documents in UTF-8. Use [normalization form NFC](http://www.w3.org/International/questions/qa-html-css-normalization).

Since vintage browsers used to have problems with a leading [byte-order mark (BOM)](http://www.w3.org/International/questions/qa-byte-order-mark) consider saving your files as UTF-8 without BOM. Do not use a BOM in includes because the BOM must not appear in the middle of a document.

## Language

Declare the language of your page content with the [lang attribute](/html/attributes/lang) on the html element. Indicate languages changes inside the document using lang attributes on elements containing the foreign phrases. For XHTML served as XML, use the xml:lang attribute. For XHTML1.x and polyglot HTML5, use both attributes with the same value.

As values, use language tags from the [IANA Language Subtag Registry](http://www.iana.org/assignments/language-subtag-registry).

Language information is useful for assistive technologies like screen readers, for spell checkers etc. It is mandatory for automatic hyphenation using the CSS property [hyphens](/css/properties/hyphens). [Why use the language attribute?](http://www.w3.org/International/questions/qa-lang-why)

Use the [translate attribute](/html/attributes/translate) to indicate whether content and attribute values should be translated or not.

``` {.html}
<p>The national motto of France is
<i lang="fr" translate="no">Liberté, Egalité, Fraternité</i>
(freedom, equality, brotherhood).</p>
```

 Use language negotiation on multilingual Web sites. [When to use language negotiation](http://www.w3.org/International/questions/qa-when-lang-neg)

Further reading: [Internationalization Quick Tips for the Web](http://www.w3.org/International/quicktips/Overview)

