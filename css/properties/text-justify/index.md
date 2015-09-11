---
title: text-justify
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/5671702'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`auto`'
  'Applies to': 'block containers and, optionally, inline elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'specified value'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`textJustify`'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The text-justify CSS property offers a fine level of justification control over the enclosed content, allowing for a variety of sophisticated justification models used in different language writing systems.'
tags:
  - CSS
  - Properties
uri: css/properties/text-justify

---
## <span>Summary</span>

The text-justify CSS property offers a fine level of justification control over the enclosed content, allowing for a variety of sophisticated justification models used in different language writing systems.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `auto`

Applies to
:   block containers and, optionally, inline elements

[Inherited](/css/concepts/inherited)
:   Yes

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   specified value

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `textJustify`

## <span>Syntax</span>

-   `text-justify: auto`
-   `text-justify: distribute`
-   `text-justify: inter-cluster`
-   `text-justify: inter-ideograph`
-   `text-justify: inter-word`
-   `text-justify: kashida`
-   `text-justify: none`

## <span>Values</span>

auto
:   Default. Allows the browser to determine which justification algorithm to apply.

none
:   Justification is disabled.

inter-word
:   Aligns text by increasing the space between words. This value's spacing behavior is the fastest way to make all lines of text equal in length. Its justification behavior does not affect the last line of the paragraph. This value is typically used for languages that separate words using spaces, like English or Korean.

inter-ideograph
:   Justifies lines of ideographic text, and increases or decreases both inter-ideograph and inter-word spacing. This value is typically used for CJK languages.

inter-cluster
:   Justifies lines of text that contain no inter-word spacing. This value is typically used for Southeast Asian scripts such as Thai.

distribute
:   Aligns text by increasing the space between both of words and characters. This value is sometimes used in e.g. Japanese.

kashida
:   Justifies lines of text by elongating characters at chosen points. This form of justification is intended for Arabic script languages.

## <span>Examples</span>

The first paragraph is using `inter-word` as a value of text-justify property, in English. The second one is using `distribute` in Japanese paragraph.

``` html
<p class="english">This is a simple paragraph with a altered text-justify value by inter-word.</p>

<p class="japanese">日本語では、どのように表示されるかを見てみましょう。日本語の場合にはdistributeが使用される場合があります。</p>
```

[View live example](http://code.webplatform.org/gist/5671702)

``` css
p {
    width: 300px;
    text-align: justify;
    text-align-last: justify;
}

p.english {
    text-justify: inter-word;
}

p.japanese {
    text-justify: distribute;
}
```

## <span>Related specifications</span>

[CSS Text Module Level 3](http://www.w3.org/TR/css3-text/#text-justify0)
:   W3C Working Draft

## <span>See also</span>

### <span>Other articles</span>

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `runtimeStyle`
-   `style`

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `runtimeStyle`
-   `style`
