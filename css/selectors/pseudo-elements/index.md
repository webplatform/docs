---
title: pseudo-elements
tags:
  - CSS
uri: css/selectors/pseudo-elements

---
Pseudo-elements create abstractions about the document tree beyond those specified by the document language. For instance, document languages do not offer mechanisms to access the first letter or first line of an element's content. Pseudo-elements allow authors to refer to this otherwise inaccessible information. Pseudo-elements may also provide authors a way to refer to content that does not exist in the source document (e.g., the `::before` and `::after` pseudo-elements give access to generated content).

A pseudo-element is made of two colons (`::`) followed by the name of the pseudo-element.

This `::` notation is introduced by the current document in order to establish a discrimination between pseudo-classes and pseudo-elements. For compatibility with existing style sheets, user agents must also accept the previous one-colon notation for pseudo-elements introduced in CSS levels 1 and 2 (namely, `:first-line`, `:first-letter`, `:before` and `:after`). This compatibility is not allowed for the new pseudo-elements introduced in this specification.

Only one pseudo-element may appear per selector, and if present it must appear after the sequence of simple selectors that represents the [subjects](http://www.w3.org/TR/2011/REC-css3-selectors-20110929/#subject) of the selector.

> **Note:** A future version of this specification may allow multiple pseudo-elements per selector.

Pseudo-elements selectors:

-   [::first-line](/css/selectors/pseudo-elements/::first-line)
-   [::first-letter](/css/selectors/pseudo-elements/::first-letter)
-   [::after](/css/selectors/pseudo-elements/::after)
-   [::before](/css/selectors/pseudo-elements/::before)
-   [::selection](/css/selectors/pseudo-elements/::selection) (not standard)

## <span>The `::first-line` pseudo-element</span>

The `::first-line` pseudo-element describes the contents of the first formatted line of an element.

CSS example:

``` css
p::first-line { text-transform: uppercase }
```

The above rule means "change the letters of the first line of every p element to uppercase". The selector `p::first-line` does not match any real document element. It does match a pseudo-element that conforming user agents will insert at the beginning of every `p` element.

Note that the length of the first line depends on a number of factors, including the width of the page, the font size, etc. Thus, an ordinary HTML paragraph such as:

``` html
<P>This is a somewhat long HTML
paragraph that will be broken into several
lines. The first line will be identified
by a fictional tag sequence. The other lines
will be treated as ordinary lines in the
paragraph.</P>
```

the lines of which happen to be broken as follows:

``` html
THIS IS A SOMEWHAT LONG HTML PARAGRAPH THAT
will be broken into several lines. The first
line will be identified by a fictional tag
sequence. The other lines will be treated as
ordinary lines in the paragraph.
```

This paragraph might be "rewritten" by user agents to include the fictional tag sequence for `::first-line`. This fictional tag sequence helps to show how properties are inherited.

``` html
<P><P::first-line> This is a somewhat long HTML
paragraph that </P::first-line> will be broken into several
lines. The first line will be identified
by a fictional tag sequence. The other lines
will be treated as ordinary lines in the
paragraph.</P>
```

If a pseudo-element breaks up a real element, the desired effect can often be described by a fictional tag sequence that closes and then re-opens the element. Thus, if we mark up the previous paragraph with a span element:

``` html
<P><SPAN class="test"> This is a somewhat long HTML
paragraph that will be broken into several
lines.</SPAN> The first line will be identified
by a fictional tag sequence. The other lines
will be treated as ordinary lines in the
paragraph.</P>
```

the user agent could simulate start and end tags for span when inserting the fictional tag sequence for `::first-line`.

``` html
<P><P::first-line><SPAN class="test"> This is a
somewhat long HTML
paragraph that will </SPAN></P::first-line><SPAN class="test"> be
broken into several
lines.</SPAN> The first line will be identified
by a fictional tag sequence. The other lines
will be treated as ordinary lines in the
paragraph.</P>
```

### <span>First formatted line definition in CSS</span>

In CSS, the `::first-line` pseudo-element can only have an effect when attached to a block-like container such as a block box, inline-block, table-caption, or table-cell.

The first formatted line of an element may occur inside a block-level descendant in the same flow (i.e., a block-level descendant that is not out-of-flow due to floating or positioning). For example, the first line of the `DIV` in

This line...

</code> is the first line of the `P` (assuming that both `P` and `DIV` are block-level). The first line of a table-cell or inline-block cannot be the first formatted line of an ancestor element. Thus, in

Hello
Goodbye

etcetera

</code> the first formatted line of the `DIV` is not the line "Hello".

> **Note:** Note that the first line of the `p` in this fragment:
>
>     <p><br>First...
>
> doesn't contain any letters (assuming the default style for br in HTML 4). The word "First" is not on the first formatted line.

A UA should act as if the fictional start tags of the `::first-line` pseudo-elements were nested just inside the innermost enclosing block-level element. (Since CSS1 and CSS2 were silent on this case, authors should not rely on this behavior.) For example, the fictional tag sequence for

``` html
<DIV>
  <P>First paragraph</P>
  <P>Second paragraph</P>
</DIV>
```

 is

``` html
<DIV>
  <P><DIV::first-line><P::first-line>First paragraph</P::first-line></DIV::first-line></P>
  <P><P::first-line>Second paragraph</P::first-line></P>
</DIV>
```

 The `::first-line` pseudo-element is similar to an inline-level element, but with certain restrictions. The following CSS properties apply to a `::first-line` pseudo-element: font properties, color property, background properties, ‘`word-spacing`’, ‘`letter-spacing`’, ‘`text-decoration`’, ‘`vertical-align`’, ‘`text-transform`’, ‘`line-height`’. UAs may apply other properties as well.

During CSS inheritance, the portion of a child element that occurs on the first line only inherits properties applicable to the `::first-line` pseudo-element from the `::first-line` pseudo-element. For all other properties inheritence is from the non-pseudo-element parent of the first line pseudo element. (The portion of a child element that does not occur on the first line always inherits from the parent of that child.)

## <span>The `::first-letter` pseudo-element</span>

The `::first-letter` pseudo-element represents the first letter of an element, if it is not preceded by any other content (such as images or inline tables) on its line. The `::first-letter` pseudo-element may be used for "initial caps" and "drop caps", which are common typographical effects.

Punctuation (i.e, characters defined in Unicode in the "open" (Ps), "close" (Pe), "initial" (Pi). "final" (Pf) and "other" (Po) punctuation classes), that precedes or follows the first letter should be included. [UNICODE](http://www.w3.org/TR/2011/REC-css3-selectors-20110929/#UNICODE)

The `::first-letter` also applies if the first letter is in fact a digit, e.g., the "6" in "67 million dollars is a lot of money."

> **Note:** In some cases the `::first-letter` pseudo-element should include more than just the first non-punctuation character on a line. For example, combining characters must be kept with their base character. Additionally, some languages may have specific rules about how to treat certain letter combinations. The UA definition of `::first-letter` should include at least the default grapheme cluster as defined by UAX29 and may include more than that as appropriate. In Dutch, for example, if the letter combination "ij" appears at the beginning of an element, both letters should be considered within the `::first-letter` pseudo-element. [UAX29](http://www.w3.org/TR/2011/REC-css3-selectors-20110929/#UAX29)

If the letters that would form the ::first-letter are not in the same element, such as "‘T" in

    <p>'<em>T...

, the UA may create a `::first-letter` pseudo-element from one of the elements, both elements, or simply not create a pseudo-element.

Similarly, if the first letter(s) of the block are not at the start of the line (for example due to bidirectional reordering), then the UA need not create the pseudo-element(s).

The following CSS and HTML example illustrates how overlapping pseudo-elements may interact. The first letter of each P element will be green with a font size of ’`24pt`'. The rest of the first formatted line will be ‘`blue`’ while the rest of the paragraph will be ‘`red`’.

``` css
p { color: red; font-size: 12pt }
p::first-letter { color: green; font-size: 200% }
p::first-line { color: blue }
```

``` html
<P>Some text that ends up on two lines</P>
```

Assuming that a line break will occur before the word "ends", the fictional tag sequence for this fragment might be:

``` html
<P>
<P::first-line>
<P::first-letter>
S
</P::first-letter>ome text that
</P::first-line>
ends up on two lines
</P>
```

Note that the `::first-letter` element is inside the `::first-line` element. Properties set on `::first-line` are inherited by `::first-letter`, but are overridden if the same property is set on `::first-letter`.

The first letter must occur on the first formatted line. For example, in this HTML fragment:

    <p><br>First...

the first line doesn't contain any letters and `::first-letter` doesn't match anything (assuming the default style for br in HTML 4). In particular, it does not match the "F" of "First."