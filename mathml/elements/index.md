---
title: 'MathML Elements'
notes:
  - 'Make sure that all child element pages are ready before setting a status'
summary: 'Index page for MathML elements.'
tags:
  - API_Listings
  - MathML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - mathml/elements/maligngroup
    - mathml/elements/malignmark
    - mathml/elements/mlabeledtr
    - mathml/elements/mtable
    - mathml/elements/mtd
    - mathml/elements/mtr
    - mathml/elements/mover
    - mathml/elements/msub
    - mathml/elements/msubsup
    - mathml/elements/msup
    - mathml/elements/munder
    - mathml/elements/munderover
    - mathml/elements/mlongdiv
    - mathml/elements/mscarries
    - mathml/elements/mscarry
    - mathml/elements/msgroup
    - mathml/elements/msline
    - mathml/elements/msrow
    - mathml/elements/mstack
    - mathml/elements/semantics
    - mathml/elements/annotation
    - mathml/elements/annotation-xml
uri: mathml/elements

---
## Summary

Index page for MathML elements.

[maction](/mathml/elements/maction)
:   The MathML **maction** element provides a possibility to bind actions to (sub-) expressions.

    The action itself is specified by the actiontype attribute, which accepts several values. To specify which child elements are addressed by the action, you can make use of the selection attribute.

[math](/mathml/elements/math)
:   The top-level element in MathML is **\<math\>**. Every valid MathML instance must be wrapped in \<math\> tags. In addition you must not nest a second \<math\> element in another, but you can have an arbitrary number of other child elements in it.

[menclose](/mathml/elements/menclose)
:   The MathML **menclose** element renders its content inside an enclosing notation specified by the notation attribute.

[merror](/mathml/elements/merror)
:   The MathML **merror** element is used to display contents as error messages. In Firefox this error message is rendered similar to the typical XML error message. Note that this error is not thrown when your MathML markup is wrong or not well-formed XML. You will still get an XML parsing error (in case of the XHTML notation of MathML), which has nothing to do with merror.

[mfenced](/mathml/elements/mfenced)
:   The MathML **mfenced** element provides the possibility to add custom opening and closing parentheses (such as brackets) and separators (such as commas or semicolons) to an expression.

[mfrac](/mathml/elements/mfrac)
:   The MathML **mfrac** element is used to display fractions.

[mglyph](/mathml/elements/mglyph)
:   The MathML **mglyph** element is used to display non-standard symbols where existing Unicode characters are not available. It may be used within token elements.

[mi](/mathml/elements/mi)
:   The MathML **mi** element indicates that the content should be rendered as an identifier such as function names, variables or symbolic constants. You can also have arbitrary text in it to mark up terms.

[mmultiscripts](/mathml/elements/mmultiscripts)
:   The MathML **mmultiscripts** element allows you to create tensor-like objects.

[mn](/mathml/elements/mn)
:   The MathML **mn** element represents a numeric literal which is normally a sequence of digits with a possible separator (a dot or a comma). However, it is also allowed to have arbitrary text in it which is actually a numeric quantity, for example "eleven".

[mpadded](/mathml/elements/mpadded)
:   The MathML **mpadded** element is used to add extra padding and to set the general adjustment of position and size of enclosed contents.

[mphantom](/mathml/elements/mphantom)
:   The MathML **mphantom** element is rendered invisibly, but dimensions (such as height, width, and baseline position) are still kept.

[mroot](/mathml/elements/mroot)
:   The MathML **mroot** element is used to display roots with an explicit index. Two arguments are accepted, which leads to the syntax: \<mroot\> base index \</mroot\>.

[mrow](/mathml/elements/mrow)
:   The MathML **mrow** element is used to group sub-expressions, which usually contain one or more operators with their respective operands (such as [mi](/mathml/elements/mi) and [mn](/mathml/elements/mn)). This element renders as a horizontal row containing its arguments.

[ms](/mathml/elements/ms)
:   The MathML **ms** element represents a string literal meant to be interpreted by programming languages and computer algebra systems.

[mspace](/mathml/elements/mspace)
:   The MathML **mspace** element is used to display a blank space, whose size is set by its attributes.

[msqrt](/mathml/elements/msqrt)
:   The MathML **msqrt** element is used to display square roots (no index is displayed). The square root accepts only one argument, which leads to the following syntax: \<msqrt\> base \</msqrt\>.

[mstyle](/mathml/elements/mstyle)
:   The MathML **mstyle** element is used change the style of its children. It accepts all attributes of all MathML presentation elements with some exceptions and additional attributes listed below.

[mtext](/mathml/elements/mtext)
:   The MathML **mtext** element is used to render arbitrary text with no notational meaning, such as comments or annotations.

    To display text *with* notational meaning, use [mi](/mathml/elements/mi) and [mo](/mathml/elements/mo) instead.

## The root element

-   [math](/mathml/elements/math)

## Presentation markup

For the presentation of a mathematical formulas.

### Enlivening expressions

-   [maction](/mathml/elements/maction)

### General Layout Schemata

-   [menclose](/mathml/elements/menclose)
-   [merror](/mathml/elements/merror)
-   [mfenced](/mathml/elements/mfenced)
-   [mfrac](/mathml/elements/mfrac)
-   [mglyph](/mathml/elements/mglyph)
-   [mpadded](/mathml/elements/mpadded)
-   [mphantom](/mathml/elements/mphantom)
-   [mroot](/mathml/elements/mroot)
-   [mrow](/mathml/elements/mrow)
-   [msqrt](/mathml/elements/msqrt)
-   [mstyle](/mathml/elements/mstyle)

### Token Elements

-   [mi](/mathml/elements/mi)
-   [mn](/mathml/elements/mn)
-   [mo](/mathml/elements/mo)
-   [ms](/mathml/elements/ms)
-   [mspace](/mathml/elements/mspace)
-   [mtext](/mathml/elements/mtext)

### Tabular Math

-   [maligngroup](/w/index.php?title=mathml/elements/maligngroup&action=edit&redlink=1)
-   [malignmark](/w/index.php?title=mathml/elements/malignmark&action=edit&redlink=1)
-   [mlabeledtr](/w/index.php?title=mathml/elements/mlabeledtr&action=edit&redlink=1)
-   [mtable](/w/index.php?title=mathml/elements/mtable&action=edit&redlink=1)
-   [mtd](/w/index.php?title=mathml/elements/mtd&action=edit&redlink=1)
-   [mtr](/w/index.php?title=mathml/elements/mtr&action=edit&redlink=1)

### Script and Limit Schemata

-   [mmultiscripts](/mathml/elements/mmultiscripts)
-   [mover](/w/index.php?title=mathml/elements/mover&action=edit&redlink=1)
-   [msub](/w/index.php?title=mathml/elements/msub&action=edit&redlink=1)
-   [msubsup](/w/index.php?title=mathml/elements/msubsup&action=edit&redlink=1)
-   [msup](/w/index.php?title=mathml/elements/msup&action=edit&redlink=1)
-   [munder](/w/index.php?title=mathml/elements/munder&action=edit&redlink=1)
-   [munderover](/w/index.php?title=mathml/elements/munderover&action=edit&redlink=1)

### Elementary Math

-   [mlongdiv](/w/index.php?title=mathml/elements/mlongdiv&action=edit&redlink=1)
-   [mscarries](/w/index.php?title=mathml/elements/mscarries&action=edit&redlink=1)
-   [mscarry](/w/index.php?title=mathml/elements/mscarry&action=edit&redlink=1)
-   [msgroup](/w/index.php?title=mathml/elements/msgroup&action=edit&redlink=1)
-   [msline](/w/index.php?title=mathml/elements/msline&action=edit&redlink=1)
-   [msrow](/w/index.php?title=mathml/elements/msrow&action=edit&redlink=1)
-   [mstack](/w/index.php?title=mathml/elements/mstack&action=edit&redlink=1)

## Other elements

-   [semantics](/w/index.php?title=mathml/elements/semantics&action=edit&redlink=1)
-   [annotation](/w/index.php?title=mathml/elements/annotation&action=edit&redlink=1)
-   [annotation-xml](/w/index.php?title=mathml/elements/annotation-xml&action=edit&redlink=1)

## See also

-   [List of HTML Elements](/html/elements)
-   [List of SVG Elements](/svg/elements)
