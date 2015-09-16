---
title: ::first-letter
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'https://gist.github.com/6cbbb246cdbcf6c2bfaf'
  - 'https://gist.github.com/5257e9b2d1e11631d608'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: "Represents the first letter of an element, if it is not preceded by any other content (such as images or inline tables) on its line. The\_::first-letter pseudo-element may be used for &quot;initial caps&quot; and &quot;drop caps&quot;, which are common typographical effects."
tags:
  - CSS
  - Selectors
uri: 'css/selectors/pseudo-elements/::first-letter'

---
## Summary

Represents the first letter of an element, if it is not preceded by any other content (such as images or inline tables) on its line. The ::first-letter pseudo-element may be used for &quot;initial caps&quot; and &quot;drop caps&quot;, which are common typographical effects.

### Syntax

``` css
::first-letter {}
```

### Usage

The ::first-letter pseudo-element selects the first letter or digit of the first line of a block. Some languages require two letters to be capitalised (digraphs) which are currently very poorly supported by browsers.

The ::first-letter pseudo-element can be attached to block-level elements. It can be attached to inline elements if you set the corresponding display property to block.

## Examples

The following CSS will create "initial caps" by doubling the size of the first letter of any paragraph.

``` css
p::first-letter {
   font-size: 200%;
}
```

[View live example](https://code.webplatform.org/gist/6cbbb246cdbcf6c2bfaf)

The following CSS will create a drop capital spanning about two lines.

``` css
p::first-letter {
    float: left;
    font-size: 300%;
}
```

[View live example](https://code.webplatform.org/gist/5257e9b2d1e11631d608)

## Notes

Only the following properties apply to the ::first-letter pseudo-element: [**background**](/css/properties/background), [**border**](/css/properties/border), [**color**](/css/properties/color), [**font**](/css/properties/font), [**font-family**](/css/properties/font-family), [**font-size**](/css/properties/font-size), [**font-style**](/css/properties/font-style), [**font-variant**](/css/fonts/font-variant), [**font-weight**](/css/properties/font-weight), [**float**](/css/properties/float), [**line-height**](/css/properties/line-height), [**margin**](/css/properties/margin), [**padding**](/css/properties/padding), [**text-decoration**](/css/properties/text-decoration), [**text-shadow**](/css/properties/text-shadow), [**text-transform**](/css/properties/text-transform), [**vertical-align**](/css/properties/vertical-align) (if 'float' is set to 'none'), and [**word-spacing**](/css/text/word-spacing/word-spacing)

## Related specifications

[CSS 2.1 Selectors](http://www.w3.org/TR/CSS2/selector.html#first-letter)
:   W3C Recommendation

[CSS 3 Selectors](http://www.w3.org/TR/css3-selectors/#first-letter)
:   W3C Recommendation
