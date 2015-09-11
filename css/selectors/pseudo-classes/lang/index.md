---
title: :lang(c)
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs title, summary, spec reference, standardization status, remove topic cluster flags'
readiness: 'Not Ready'
summary: 'The :lang(c) pseudo selector applies to documents that specifies the lang attribute to an HTML element. This allows to style based on which language (and/or dialect) a given section is written into.'
tags:
  - CSS
  - Selectors
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - selection
uri: 'css/selectors/pseudo-classes/:lang(c)'

---
## <span>Summary</span>

The :lang(c) pseudo selector applies to documents that specifies the lang attribute to an HTML element. This allows to style based on which language (and/or dialect) a given section is written into.

 If the document language specifies how the human language of an element is determined, it is possible to write selectors that represent an element based on its language. For example, in HTML [[HTML401](http://www.w3.org/TR/2011/REC-css3-selectors-20110929/#HTML401)], the language is determined by a combination of the `lang` attribute and possibly information from the `meta` elements or the protocol (such as HTTP headers). XML uses an attribute called `xml:lang`, and there may be other document language-specific methods for determining the language.

The pseudo-class `:lang(C)` represents an element that is in language `C`. Whether an element is represented by a `:lang()` selector is based solely on the element's language value (normalized to BCP 47 syntax if necessary) being equal to the identifier `C`, or beginning with the identifier `C` immediately followed by "`-`" (U+002D). The matching of `C` against the element's language value is performed case-insensitively. The identifier C does not have to be a valid language name.

`C` must be a valid CSS [identifier](http://www.w3.org/TR/CSS21/syndata.html#value-def-identifier) [[CSS21](http://www.w3.org/TR/2011/REC-css3-selectors-20110929/#CSS21)] and must not be empty. (Otherwise, the selector is invalid.)

> **Note:** It is [[recommended](http://www.w3.org/TR/2011/REC-css3-selectors-20110929/#lang-pseudo)] that documents and protocols indicate language using codes from BCP 47 [[BCP47](http://www.w3.org/TR/2011/REC-css3-selectors-20110929/#BCP47)] or its successor, and by means of "`xml:lang`" attributes in the case of XML-based documents [[XML10](http://www.w3.org/TR/2011/REC-css3-selectors-20110929/#XML10)]. See "[Two-letter or three-letter language codes.](http://www.w3.org/International/questions/qa-lang-2or3.htmlFAQ:)"

 The value of *C* should be a language code that is indicated by [RFC3066: Tags for the Identification of Languages](http://www.ietf.org/rfc/rfc3066.txt).

If *C* is empty or invalid, the selector will have no effect.

### <span>Syntax</span>


     selector:lang(C) { /* ... */ }


### <span>Parameters</span>

*selector*
:   A CSS simple selector
*C*
:   Language code as specified in [RFC3066: Tags for the Identification of Languages](http://www.ietf.org/rfc/rfc3066.txt)

## <span>Examples</span>

The following code example uses the **:lang(C)** pseudo-class to apply a color to any **p** elements that are explicitly given a language value of "en" (or a hyphen-separated subset thereof). The first paragraph gets "en-us" (a subset of "en") and thus turns green.

``` html
<!DOCTYPE html>
  <html>
  <head>
  <meta http-equiv="X-UA-Compatible" content="IE=8"/>
  <title>:lang pseudo-class</title>
  <style type="text/css">
  p:lang(en) {
    color: green;
  }
  </style>
  </head>
  <body>
  <div class=body>

    <h1>:lang(C) Sample</h1>

    <!-- This paragraph gets "en-us" (a subset of "en") and thus turns green. -->
    <p lang="en-us">This paragraph's language is set to "en-us", so it's green.</p>
    <!-- This paragraph has no language value and thus does not turn green. -->
    <p>This paragraph has no language attribute, so it doesn't turn green.</p>
    <!-- This paragraph is actually a div; therefore, even though its language value
        is "en-us", it does not turn green. -->
    <div lang="en-us">This div's language is set to "en-us", but this page's :lang
        pseudo-class only applies to paragraphs, so it doesn't turn green.</div>

  </div>
  </body>
  </html>
```

How to declare a full HTML document body language

``` html
<body>
    <p>This text is written in english, but <span lang=fr>cette section ci est écrite en français</span>.</p>
  </body>
```

The two following selectors represent an HTML document that is in Belgian French or German. The two next selectors represent q quotations in an arbitrary element in Belgian French or German.

``` css
html:lang(fr-be)
  html:lang(de)
  :lang(fr-be) > q
  :lang(de) > q
```

Match all of the listed language codes (and any corresponding hyphen-separated substrings of language codes) that are known to have text orientation from **right to left** (see the "rtl" value at the *direction* property).

``` css
html:lang(ar),
  html:lang(dv),
  html:lang(fa),
  html:lang(he),
  html:lang(ku-Arab),
  html:lang(pa-Arab),
  html:lang(prs),
  html:lang(ps),
  html:lang(sd-Arab),
  html:lang(syr),
  html:lang(ug),
  html:lang(ur),
  html:lang(qps-plocm) {
     direction: rtl;
  }
```

## <span>Related specifications</span>

[CSS 2.1](http://www.w3.org/TR/CSS2/selector.html#lang)
:   W3C Recommendation

## <span>See also</span>

### <span>Related articles</span>

#### <span>Pseudo-Classes</span>

-   [:target pseudo-class selector](/CSS/Selectors/pseudo-classes/:target)

-   [:-ms-input-placeholder](/css/selectors/pseudo-classes/:-ms-input-placeholder)

-   [:checked](/css/selectors/pseudo-classes/:checked)

-   [:disabled](/css/selectors/pseudo-classes/:disabled)

-   [:empty](/css/selectors/pseudo-classes/:empty)

-   [:enabled](/css/selectors/pseudo-classes/:enabled)

-   [:first-child](/css/selectors/pseudo-classes/:first-child)

-   [:first-of-type](/css/selectors/pseudo-classes/:first-of-type)

-   [:focus](/css/selectors/pseudo-classes/:focus)

-   [:in-range](/css/selectors/pseudo-classes/:in-range)

-   [:indeterminate](/css/selectors/pseudo-classes/:indeterminate)

-   [:invalid](/css/selectors/pseudo-classes/:invalid)

-   **:lang(c)**

-   [:last-of-type](/css/selectors/pseudo-classes/:last-of-type)

-   [:nth-child(n)](/css/selectors/pseudo-classes/:nth-child(n))

-   [:nth-last-child(n)](/css/selectors/pseudo-classes/:nth-last-child(n))

-   [:nth-last-of-type(n)](/css/selectors/pseudo-classes/:nth-last-of-type(n))

-   [:nth-of-type(n)](/css/selectors/pseudo-classes/:nth-of-type(n))

-   [:only-child](/css/selectors/pseudo-classes/:only-child)

-   [:only-of-type](/css/selectors/pseudo-classes/:only-of-type)

-   [:optional](/css/selectors/pseudo-classes/:optional)

-   [:required](/css/selectors/pseudo-classes/:required)

-   [:root](/css/selectors/pseudo-classes/:root)

-   [:target](/css/selectors/pseudo-classes/:target)

-   [:valid](/css/selectors/pseudo-classes/:valid)

#### <span>Selectors</span>

-   [querySelectorAll](/css/selectors_api/querySelectorAll)

-   [ID](/css/selectors/ID)

-   [Namespaced](/css/selectors/Namespaced)

-   [Universal](/css/selectors/Universal)

-   [equality](/css/selectors/attributes/equality)

-   [Attribute selector](/css/selectors/attributes/existence)

-   [hyphen](/css/selectors/attributes/hyphen)

-   [prefix](/css/selectors/attributes/prefix)

-   [substring](/css/selectors/attributes/substring)

-   [suffix](/css/selectors/attributes/suffix)

-   [whitespace](/css/selectors/attributes/whitespace)

-   [:-ms-input-placeholder](/css/selectors/pseudo-classes/:-ms-input-placeholder)

-   [:checked](/css/selectors/pseudo-classes/:checked)

-   [:disabled](/css/selectors/pseudo-classes/:disabled)

-   [:empty](/css/selectors/pseudo-classes/:empty)

-   [:enabled](/css/selectors/pseudo-classes/:enabled)

-   [:first-child](/css/selectors/pseudo-classes/:first-child)

-   [:first-of-type](/css/selectors/pseudo-classes/:first-of-type)

-   [:focus](/css/selectors/pseudo-classes/:focus)

-   [:in-range](/css/selectors/pseudo-classes/:in-range)

-   [:indeterminate](/css/selectors/pseudo-classes/:indeterminate)

-   [:invalid](/css/selectors/pseudo-classes/:invalid)

-   **:lang(c)**

-   [:last-of-type](/css/selectors/pseudo-classes/:last-of-type)

-   [:nth-child(n)](/css/selectors/pseudo-classes/:nth-child(n))

-   [:nth-last-child(n)](/css/selectors/pseudo-classes/:nth-last-child(n))

-   [:nth-last-of-type(n)](/css/selectors/pseudo-classes/:nth-last-of-type(n))

-   [:nth-of-type(n)](/css/selectors/pseudo-classes/:nth-of-type(n))

-   [:only-child](/css/selectors/pseudo-classes/:only-child)

-   [:only-of-type](/css/selectors/pseudo-classes/:only-of-type)

-   [:optional](/css/selectors/pseudo-classes/:optional)

-   [:required](/css/selectors/pseudo-classes/:required)

-   [:root](/css/selectors/pseudo-classes/:root)

-   [:target](/css/selectors/pseudo-classes/:target)

-   [:valid](/css/selectors/pseudo-classes/:valid)

-   [::selection](/w/index.php?title=selection&action=edit&redlink=1)

-   [type](/css/selectors/type)

### <span>External resources</span>

-   Language code as specified in [RFC3066: Tags for the Identification of Languages](http://www.ietf.org/rfc/rfc3066.txt)
-   [Styling by language](http://www.w3.org/International/techniques/authoring-html#langstyle)
