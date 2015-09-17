---
title: 'CSS Selectors'
readiness: 'Ready to Use'
summary: "A Selector represents a structure. This structure can be used as a condition (e.g. in a CSS rule) that determines which elements a selector matches in the document tree, or as a flat description of the HTML or XML fragment corresponding to that structure.\n"
tags:
  - Basic_Pages
  - CSS
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'css/selectors/pseudo-classes/:lang'
uri: css/selectors

---
## Summary

A Selector represents a structure. This structure can be used as a condition (e.g. in a CSS rule) that determines which elements a selector matches in the document tree, or as a flat description of the HTML or XML fragment corresponding to that structure.

Selectors may range from simple element names to rich contextual representations.

## CSS Selector Reference

### Type Selector

-   [`elementname`](/css/selectors/type)

### Universal Selector

-   [`*`](/css/selectors/universal_selector)

### [Attribute Selector](/css/selectors/attribute_selector)

-   [attributename][[attributename]](/css/selectors/attributes/existence)
-   [attributename="val"][[attributename="val"]](/css/selectors/attributes/equality)
-   [attributename\~="val"][[attributename\~="val"]](/css/selectors/attributes/whitespace)
-   [attributename|="val"][[attributename|="val"]](/css/selectors/attributes/hyphen)
-   [attributename\^="val"][[attributename\^="val"]](/css/selectors/attributes/prefix)
-   [attributename\$="val"][[attributename\$="val"]](/css/selectors/attributes/suffix)
-   [attributename\*="val"][[attributename\*="val"]](/css/selectors/attributes/substring)

### Class Selector

-   [`.classname`](/css/selectors/class_selector)

### ID Selector

-   [`#idname`](/css/selectors/id_selector)

### Pseudo-classes

#### [Dynamic pseudo-classes](/css/selectors/pseudo-classes)

-   :link[:link](/css/selectors/pseudo-classes/:link)
-   :visited[:visited](/css/selectors/pseudo-classes/:visited)
-   :hover[:hover](/css/selectors/pseudo-classes/:hover)
-   :active[:active](/css/selectors/pseudo-classes/:active)
-   :focus[:focus](/css/selectors/pseudo-classes/:focus)

#### The target pseudo-class

-   [`:target`](/css/selectors/pseudo-classes/:target)

#### The language pseudo-class

-   [`:lang`](/w/index.php?title=css/selectors/pseudo-classes/:lang&action=edit&redlink=1)

#### [The UI element states pseudo-classes](/css/selectors/pseudo-classes/ui_element_states_pseudo-classes)

-   :enabled[:enabled](/css/selectors/pseudo-classes/:enabled)
-   :disabled[:disabled](/css/selectors/pseudo-classes/:disabled)
-   :checked[:checked](/css/selectors/pseudo-classes/:checked)

#### [Structural pseudo-classes](/css/selectors/pseudo-classes/Structural_pseudo-classes)

-   [`:root`](/css/selectors/pseudo-classes/Structural_pseudo-classes#:root_pseudo-class)
-   [`:nth-child`](/css/selectors/pseudo-classes/Structural_pseudo-classes#:nth-child.28.29_pseudo-class)
-   [`:nth-last-child`](/css/selectors/pseudo-classes/Structural_pseudo-classes#:nth-last-child.28.29_pseudo-class)
-   [`:nth-of-type`](/css/selectors/pseudo-classes/Structural_pseudo-classes#:nth-of-type.28.29_pseudo-class)
-   [`:nth-last-of-type`](/css/selectors/pseudo-classes/Structural_pseudo-classes#:nth-last-of-type.28.29_pseudo-class)
-   [`:first-child`](/css/selectors/pseudo-classes/Structural_pseudo-classes#:first-child_pseudo-class)
-   [`:last-child`](/css/selectors/pseudo-classes/Structural_pseudo-classes#:last-child_pseudo-class)
-   [`:first-of-type`](/css/selectors/pseudo-classes/Structural_pseudo-classes#:first-of-type_pseudo-class)
-   [`:last-of-type`](/css/selectors/pseudo-classes/Structural_pseudo-classes#:last-of-type_pseudo-class)
-   [`:only-child`](/css/selectors/pseudo-classes/Structural_pseudo-classes#:only-child_pseudo-class)
-   [`:only-of-type`](/css/selectors/pseudo-classes/Structural_pseudo-classes#:only-of-type_pseudo-class)
-   [`:empty`](/css/selectors/pseudo-classes/Structural_pseudo-classes#:empty_pseudo-class)

#### The negation pseudo-class

-   [`:not`](/css/selectors/pseudo-classes/:not)

### Pseudo-elements

-   [`::first-line`](/css/selectors/pseudo-elements/::first-line)
-   [`::first-letter`](/css/selectors/pseudo-elements/::first-letter)
-   [`::before`](/css/selectors/pseudo-elements/::before)
-   [`::after`](/css/selectors/pseudo-elements/::after)

### Combinators

#### Descendant combinator

-   [`A B`](/css/selectors/combinators/descendant)

#### Child combinator

-   [`A > B`](/css/selectors/combinators/child)

#### Adjacent sibling combinator

-   [`A + B`](/css/selectors/combinators/adjacent_sibling)

#### General sibling combinator

-   [`A ~ B`](/css/selectors/combinators/general_sibling)

## Case sensitivity

All Selectors syntax is case-insensitive within the ASCII range (i.e. [a-z] and [A-Z] are equivalent), except for parts that are not under the control of Selectors. The case sensitivity of document language element names, attribute names, and attribute values in selectors depends on the document language. For example, in HTML, element names are case-insensitive, but in XML, they are case-sensitive. Case sensitivity of namespace prefixes is defined in [CSS3NAMESPACE](http://www.w3.org/TR/2011/REC-css3-selectors-20110929/#CSS3NAMESPACE).

## Selector syntax

A selector is a chain of one or more sequences of simple selectors separated by combinators. One pseudo-element may be appended to the last sequence of simple selectors in a selector. A sequence of simple selectors is a chain of simple selectors that are not separated by a combinator. It always begins with a type selector or a universal selector. No other type selector or universal selector is allowed in the sequence.

A simple selector is either a type selector, universal selector, attribute selector, class selector, ID selector, or pseudo-class.

Combinators are: whitespace, "greater-than sign" (U+003E, \>), "plus sign" (U+002B, +) and "tilde" (U+007E, \~). White space may appear between a combinator and the simple selectors around it. Only the characters "space" (U+0020), "tab" (U+0009), "line feed" (U+000A), "carriage return" (U+000D), and "form feed" (U+000C) can occur in whitespace. Other space-like characters, such as "em-space" (U+2003) and "ideographic space" (U+3000), are never part of whitespace.

The elements of a document tree that are represented by a selector are the subjects of the selector. A selector consisting of a single sequence of simple selectors represents any element satisfying its requirements. Prepending another sequence of simple selectors and a combinator to a sequence imposes additional matching constraints, so the subjects of a selector are always a subset of the elements represented by the last sequence of simple selectors.

An empty selector, containing no sequence of simple selectors and no pseudo-element, is an invalid selector. Characters in Selectors can be escaped with a backslash according to the same escaping rules as CSS. [CSS21](http://www.w3.org/TR/2011/REC-css3-selectors-20110929/#CSS21).

Certain selectors support namespace prefixes. The mechanism by which namespace prefixes are declared should be specified by the language that uses Selectors. If the language does not specify a namespace prefix declaration mechanism, then no prefixes are declared. In CSS, namespace prefixes are declared with the @namespace rule. [CSS3NAMESPACE](http://www.w3.org/TR/2011/REC-css3-selectors-20110929/#CSS3NAMESPACE)

## Groups of selectors

A comma-separated list of selectors represents the union of all elements selected by each of the individual selectors in the list. (A comma is U+002C.) For example, in CSS when several selectors share the same declarations, they may be grouped into a comma-separated list. White space may appear before and/or after the comma.

In this example, we condense three rules with identical declarations into one. Thus,

``` css
h1 { font-family: sans-serif }
h2 { font-family: sans-serif }
h3 { font-family: sans-serif }
```

is equivalent to:

``` css
h1, h2, h3 { font-family: sans-serif }
```

**Warning**: the equivalence is true in this example because all the selectors are valid selectors. If just one of these selectors were invalid, the entire group of selectors would be invalid. This would invalidate the rule for all three heading elements, whereas in the former case only one of the three individual heading rules would be invalidated.

Invalid CSS example:

``` css
h1 { font-family: sans-serif }
h2..foo { font-family: sans-serif }
h3 { font-family: sans-serif }
```

is not equivalent to:

``` css
h1, h2..foo, h3 { font-family: sans-serif }
```

because the above selector (h1, h2..foo, h3) is entirely invalid and the entire style rule is dropped. (When the selectors are not grouped, only the rule for h2..foo is dropped.)

## See also

### Related topics

-   [Using Selectors Tutorial](/tutorials/using_selectors)
-   [CSS Educational Materials for Beginners](/css/tutorials)
-   [CSS Properties Reference](/css/properties)

### Selector list

<table class="mw-prefixindex-list-table">
<tr>
<td>
[css/selectors/-ms-scrollbar-shadow-color](/css/selectors/-ms-scrollbar-shadow-color)

</td>
<td>
[css/selectors/ID](/css/selectors/ID)

</td>
<td>
[css/selectors/Namespaced](/css/selectors/Namespaced)

</td>
</tr>
<tr>
<td>
[css/selectors/Type](/css/selectors/Type)

</td>
<td>
[css/selectors/Universal](/css/selectors/Universal)

</td>
<td>
[css/selectors/attribute selector](/css/selectors/attribute_selector)

</td>
</tr>
<tr>
<td>
[css/selectors/attributes/equality](/css/selectors/attributes/equality)

</td>
<td>
[css/selectors/attributes/existence](/css/selectors/attributes/existence)

</td>
<td>
[css/selectors/attributes/hyphen](/css/selectors/attributes/hyphen)

</td>
</tr>
<tr>
<td>
[css/selectors/attributes/prefix](/css/selectors/attributes/prefix)

</td>
<td>
[css/selectors/attributes/substring](/css/selectors/attributes/substring)

</td>
<td>
[css/selectors/attributes/suffix](/css/selectors/attributes/suffix)

</td>
</tr>
<tr>
<td>
[css/selectors/attributes/whitespace](/css/selectors/attributes/whitespace)

</td>
<td>
[css/selectors/border-image](/css/selectors/border-image)

</td>
<td>
[css/selectors/class](/css/selectors/class)

</td>
</tr>
<tr>
<td>
[css/selectors/class selector](/css/selectors/class_selector)

</td>
<td>
[css/selectors/combinators/adjacent sibling](/css/selectors/combinators/adjacent_sibling)

</td>
<td>
[css/selectors/combinators/child](/css/selectors/combinators/child)

</td>
</tr>
<tr>
<td>
[css/selectors/combinators/descendant](/css/selectors/combinators/descendant)

</td>
<td>
[css/selectors/combinators/general sibling](/css/selectors/combinators/general_sibling)

</td>
<td>
[css/selectors/cursor](/css/selectors/cursor)

</td>
</tr>
<tr>
<td>
[css/selectors/id selector](/css/selectors/id_selector)

</td>
<td>
[css/selectors/outline](/css/selectors/outline)

</td>
<td>
[css/selectors/outline-color](/css/selectors/outline-color)

</td>
</tr>
<tr>
<td>
[css/selectors/outline-style](/css/selectors/outline-style)

</td>
<td>
[css/selectors/outline-width](/css/selectors/outline-width)

</td>
<td>
[css/selectors/pseudo-classes](/css/selectors/pseudo-classes)

</td>
</tr>
<tr>
<td>
[css/selectors/pseudo-classes/:-ms-input-placeholder](/css/selectors/pseudo-classes/:-ms-input-placeholder)

</td>
<td>
[css/selectors/pseudo-classes/:active](/css/selectors/pseudo-classes/:active)

</td>
<td>
[css/selectors/pseudo-classes/:checked](/css/selectors/pseudo-classes/:checked)

</td>
</tr>
<tr>
<td>
[css/selectors/pseudo-classes/:disabled](/css/selectors/pseudo-classes/:disabled)

</td>
<td>
[css/selectors/pseudo-classes/:empty](/css/selectors/pseudo-classes/:empty)

</td>
<td>
[css/selectors/pseudo-classes/:enabled](/css/selectors/pseudo-classes/:enabled)

</td>
</tr>
<tr>
<td>
[css/selectors/pseudo-classes/:first-child](/css/selectors/pseudo-classes/:first-child)

</td>
<td>
[css/selectors/pseudo-classes/:first-of-type](/css/selectors/pseudo-classes/:first-of-type)

</td>
<td>
[css/selectors/pseudo-classes/:focus](/css/selectors/pseudo-classes/:focus)

</td>
</tr>
<tr>
<td>
[css/selectors/pseudo-classes/:hover](/css/selectors/pseudo-classes/:hover)

</td>
<td>
[css/selectors/pseudo-classes/:in-range](/css/selectors/pseudo-classes/:in-range)

</td>
<td>
[css/selectors/pseudo-classes/:indeterminate](/css/selectors/pseudo-classes/:indeterminate)

</td>
</tr>
<tr>
<td>
[css/selectors/pseudo-classes/:invalid](/css/selectors/pseudo-classes/:invalid)

</td>
<td>
[css/selectors/pseudo-classes/:lang(c)](/css/selectors/pseudo-classes/:lang(c))

</td>
<td>
[css/selectors/pseudo-classes/:last-child](/css/selectors/pseudo-classes/:last-child)

</td>
</tr>
<tr>
<td>
[css/selectors/pseudo-classes/:last-of-type](/css/selectors/pseudo-classes/:last-of-type)

</td>
<td>
[css/selectors/pseudo-classes/:link](/css/selectors/pseudo-classes/:link)

</td>
<td>
[css/selectors/pseudo-classes/:not](/css/selectors/pseudo-classes/:not)

</td>
</tr>
<tr>
<td>
[css/selectors/pseudo-classes/:nth-child(n)](/css/selectors/pseudo-classes/:nth-child(n))

</td>
<td>
[css/selectors/pseudo-classes/:nth-last-child(n)](/css/selectors/pseudo-classes/:nth-last-child(n))

</td>
<td>
[css/selectors/pseudo-classes/:nth-last-of-type(n)](/css/selectors/pseudo-classes/:nth-last-of-type(n))

</td>
</tr>
<tr>
<td>
[css/selectors/pseudo-classes/:nth-of-type(n)](/css/selectors/pseudo-classes/:nth-of-type(n))

</td>
<td>
[css/selectors/pseudo-classes/:only-child](/css/selectors/pseudo-classes/:only-child)

</td>
<td>
[css/selectors/pseudo-classes/:only-of-type](/css/selectors/pseudo-classes/:only-of-type)

</td>
</tr>
<tr>
<td>
[css/selectors/pseudo-classes/:optional](/css/selectors/pseudo-classes/:optional)

</td>
<td>
[css/selectors/pseudo-classes/:required](/css/selectors/pseudo-classes/:required)

</td>
<td>
[css/selectors/pseudo-classes/:root](/css/selectors/pseudo-classes/:root)

</td>
</tr>
<tr>
<td>
[css/selectors/pseudo-classes/:target](/css/selectors/pseudo-classes/:target)

</td>
<td>
[css/selectors/pseudo-classes/:valid](/css/selectors/pseudo-classes/:valid)

</td>
<td>
[css/selectors/pseudo-classes/:visited](/css/selectors/pseudo-classes/:visited)

</td>
</tr>
<tr>
<td>
[css/selectors/pseudo-classes/Dynamic pseudo-classes](/css/selectors/pseudo-classes/Dynamic_pseudo-classes)

</td>
<td>
[css/selectors/pseudo-classes/Structural pseudo-classes](/css/selectors/pseudo-classes/Structural_pseudo-classes)

</td>
<td>
[css/selectors/pseudo-classes/ui element states pseudo-classes](/css/selectors/pseudo-classes/ui_element_states_pseudo-classes)

</td>
</tr>
<tr>
<td>
[css/selectors/pseudo-elements](/css/selectors/pseudo-elements)

</td>
<td>
[css/selectors/pseudo-elements/::after](/css/selectors/pseudo-elements/::after)

</td>
<td>
[css/selectors/pseudo-elements/::before](/css/selectors/pseudo-elements/::before)

</td>
</tr>
<tr>
<td>
[css/selectors/pseudo-elements/::first-letter](/css/selectors/pseudo-elements/::first-letter)

</td>
<td>
[css/selectors/pseudo-elements/::first-line](/css/selectors/pseudo-elements/::first-line)

</td>
<td>
[css/selectors/pseudo-elements/::region](/css/selectors/pseudo-elements/::region)

</td>
</tr>
<tr>
<td>
[css/selectors/pseudo-elements/::selection](/css/selectors/pseudo-elements/::selection)

</td>
<td>
[css/selectors/type](/css/selectors/type)

</td>
<td>
[css/selectors/universal selector](/css/selectors/universal_selector)

</td>
</tr>
<tr>
<td>
[css/selectors/user-select](/css/selectors/user-select)

</td>
<td>
[css/selectors/zoom](/css/selectors/zoom)

</td>
</tr>
</table>
## Related specifications

[Selectors Level 3](http://www.w3.org/TR/css3-selectors/)
:   Recommendation
