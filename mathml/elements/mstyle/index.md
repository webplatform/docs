---
title: 'mstyle'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/MathML/Element/mstyle)'
compatibility:
  feature: mstyle
  topic: mathml
notes:
  - 'Fix broken links'
overview_table:
  '[DOM Interface](/dom/interface)': '[mathml](/mathml)'
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
summary: 'The MathML mstyle element is used change the style of its children. It accepts all attributes of all MathML presentation elements with some exceptions and additional attributes listed below.'
tags:
  - Markup
  - Elements
  - MathML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - mathml/elements/mstack
    - mathml/elements/mtable
    - mathml/elements/mtr
    - mathml/elements/mlabeledtr
    - mathml/elements/mtd
    - mathml/elements/maligngroup
uri: mathml/elements/mstyle

---
## Summary

The MathML mstyle element is used change the style of its children. It accepts all attributes of all MathML presentation elements with some exceptions and additional attributes listed below.

## Overview Table

[DOM Interface](/dom/interface)
:   [mathml](/mathml)

## Examples

This example demonstrates a simple usage of the mstyle element:

``` html


<math>

  <mstyle displaystyle="true" mathcolor="teal">
    <mrow>

      <munderover>
        <mo stretchy="true" form="prefix">∑</mo>
        <mrow>
          <mi>i</mi>
          <mo form="infix">=</mo>
          <mn>1</mn>
        </mrow>
        <mi>n</mi>
      </munderover>

      <mstyle displaystyle="true">
        <mfrac>
          <mn>1</mn>
          <mi>n</mi>
        </mfrac>
      </mstyle>

    </mrow>
  </mstyle>

</math>
```

</pre>

## Related specifications

[MathML 3.0](http://www.w3.org/TR/MathML3/chapter3.html#presm.mstyle)
:   W3C Recommendation

## Attributes

 decimalpoint
:   This attribute is specifying the character for the alignment point within [mstack](/w/index.php?title=mathml/elements/mstack&action=edit&redlink=1) and [mtable](/w/index.php?title=mathml/elements/mtable&action=edit&redlink=1) columns, if the `decimalpoint` value is used to specify the alignment.
 displaystyle
:   A Boolean value specifying whether more vertical space is used for displayed equations or, if set to `false`, a more compact layout is used to display formulas. The main effect is that larger versions of operators are displayed, when `displaystyle` is set to `true`. See also `largeop` and `movablelimits` on [mo](/mathml/elements/mo).
 infixlinebreakstyle
:   Specifies the default `linebreakstyle` to use for infix operators. The values `before`, `after` and `duplicate` are allowed.
 scriptlevel
:   Controls mostly the font-size. The higher the `scriptlevel`, the smaller the font size. This attribute accepts a non-negative integer, as well as a "+" or a "-" sign, which increments or decrements the current value. In addition, the `scriptlevel` attribute can never reduce the font size below `scriptminsize` in order to avoid unreadable small font sizes and depends on the multiplier specified in `scriptsizemultiplier`.
 scriptminsize
:   Specifies a minimum font size allowed due to changes in `scriptlevel`. The default value is 8pt.
 scriptsizemultiplier
:   Specifies the multiplier to be used to adjust font size due to changes in `scriptlevel`. The default value is 0.71.

The `<mstyle>` element accepts [all attributes](/mathml/attributes) of all presentation attributes with the following exceptions:

-   `height`, `depth` or `width` do not apply to [mglyph](/mathml/elements/mglyph), [mpadded](/mathml/elements/mpadded) or [mtable](/w/index.php?title=mathml/elements/mtable&action=edit&redlink=1).
-   `rowalign`, `columnalign`, or `groupalign` do not apply to [mtr](/w/index.php?title=mathml/elements/mtr&action=edit&redlink=1), [mlabeledtr](/w/index.php?title=mathml/elements/mlabeledtr&action=edit&redlink=1), [mtd](/w/index.php?title=mathml/elements/mtd&action=edit&redlink=1) or [maligngroup](/w/index.php?title=mathml/elements/maligngroup&action=edit&redlink=1).
-   `lspace` or `voffset` do not apply to [mpadded](/mathml/elements/mpadded).
-   `fontfamily` does not apply to [mglyph](/mathml/elements/mglyph).
-   `align` does not apply to [mtable](/w/index.php?title=mathml/elements/mtable&action=edit&redlink=1) or [mstack](/w/index.php?title=mathml/elements/mstack&action=edit&redlink=1).
-   `index` cannot be set on `<mstyle>`.
-   `src` and `alt` on [mglyph](/mathml/elements/mglyph) cannot be set on `<mstyle>`.
-   `actiontype` on [maction](/mathml/elements/maction) cannot be set on `<mstyle>`.
