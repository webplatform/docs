---
title: unicode-bidi
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/5708639'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`normal`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'specified value'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`unicodeBidi`'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The unicode-bidi CSS property specifies the level of embedding with respect to the bidirectional algorithm.'
tags:
  - CSS
  - Properties
uri: css/properties/unicode-bidi

---
## <span>Summary</span>

The unicode-bidi CSS property specifies the level of embedding with respect to the bidirectional algorithm.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `normal`

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   specified value

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `unicodeBidi`

## <span>Syntax</span>

-   `unicode-bidi: bidi-override`
-   `unicode-bidi: embed`
-   `unicode-bidi: normal`

## <span>Values</span>

normal
:   Default. Element does not open an additional level of embedding. For inline elements, implicit reordering works across element boundaries.

embed
:   Element opens an additional level of embedding. The value of the [**direction**](/css/properties/direction) property specifies the embedding level. Reordering is implicit inside the element.

bidi-override
:   Same as the `embed` value, except that, inside the element, reordering is strictly in sequence according to the [**direction**](/css/properties/direction) property. This value overrides the implicit bidirectional algorithm.

## <span>Examples</span>

A simple example showing multiple \<p\>s, that they have different unicode-bidi properties applied to them.

``` html
<p class="rtl">This is a paragraph using right-to-left direction.</p>

<p class="rtl" id="em">Sets the embed as the value unicode-bidi property.</p>

<p class="rtl" id="bidi">Sets the bidi-override as the value of unicode-bidi property.</p>
```

[View live example](http://code.webplatform.org/gist/5708639)

``` css
p {
    width: 300px;
    background-color: #cccccc;
}

.rtl {
    direction: rtl;
}

#em {
    unicode-bidi: embed;
}

#bidi {
    unicode-bidi: bidi-override;
}
```

## <span>Notes</span>

The `unicode-bidi` property is used with the [**direction**](/css/properties/direction) property. The Unicode bidirectional algorithm automatically reverses embedded character sequences according to their inherent direction. For example, the base direction of an English document is left-to-right. If portions of a paragraph within the document contain a language with a right-to-left reading order, the direction of that language displays correctly right-to-left. The user agent applying the bidirectional algorithm correctly reverses the language direction.

## <span>Related specifications</span>

[Cascading Style Sheets Level 2 Revision 1](http://www.w3.org/TR/CSS2/visuren.html#propdef-unicode-bidi)
:   W3C Recommendation

## <span>See also</span>

### <span>Other articles</span>

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `runtimeStyle`
-   `style`
