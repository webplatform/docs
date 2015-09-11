---
title: Structural pseudo-classes
tags:
  - CSS
uri: 'css/selectors/pseudo-classes/Structural pseudo-classes'

---
Selectors introduces the concept of structural pseudo-classes to permit selection based on extra information that lies in the document tree but cannot be represented by other simple selectors or combinators.

Standalone text and other non-element nodes are not counted when calculating the position of an element in the list of children of its parent. When calculating the position of an element in the list of children of its parent, the index numbering starts at 1.

## <span>`:root` pseudo-class</span>

The `:root` pseudo-class represents an element that is the root of the document. In HTML 4, this is always the `HTML` element.

## <span>`:nth-child()` pseudo-class</span>

The `:nth-child(an+b)` pseudo-class notation represents an element that has an+b-1 siblings before it in the document tree, for any positive integer or zero value of n, and has a parent element. For values of a and b greater than zero, this effectively divides the element's children into groups of a elements (the last group taking the remainder), and selecting the bth element of each group. For example, this allows the selectors to address every other row in a table, and could be used to alternate the color of paragraph text in a cycle of four. The a and b values must be integers (positive, negative, or zero). The index of the first child of an element is 1.

In addition to this, `:nth-child()` can take ‘`odd`’ and ‘`even`’ as arguments instead. ‘`odd`’ has the same signification as 2n+1, and ‘`even`’ has the same signification as 2n.

The argument to `:nth-child()` must match the grammar below, where INTEGER matches the token [0-9]+ and the rest of the tokenization is given by the Lexical scanner in section 10.2:

    nth
      : S* [ ['-'|'+']? INTEGER? {N} [ S* ['-'|'+'] S* INTEGER ]? |
             ['-'|'+']? INTEGER | {O}{D}{D} | {E}{V}{E}{N} ] S*
      ;

### <span>Examples:</span>

``` css
tr:nth-child(2n+1) /* represents every odd row of an HTML table */
tr:nth-child(odd)  /* same */
tr:nth-child(2n+0) /* represents every even row of an HTML table */
tr:nth-child(even) /* same */

/* Alternate paragraph colours in CSS */
p:nth-child(4n+1) { color: navy; }
p:nth-child(4n+2) { color: green; }
p:nth-child(4n+3) { color: maroon; }
p:nth-child(4n+4) { color: purple; }
```

 When the value b is preceded by a negative sign, the "`+`" character in the expression must be removed (it is effectively replaced by the "`-`" character indicating the negative value of b).

``` css
:nth-child(10n-1)  /* represents the 9th, 19th, 29th, etc, element */
:nth-child(10n+9)  /* Same */
:nth-child(10n+-1) /* Syntactically invalid, and would be ignored */
```

 When a=0, the an part need not be included (unless the b part is already omitted). When an is not included and b is non-negative, the + sign before b (when allowed) may also be omitted. In this case the syntax simplifies to :nth-child(b).

``` css
foo:nth-child(0n+5)   /* represents an element foo that is the 5th child of its parent element */
foo:nth-child(5)      /* same */
```

 When a=1, or a=-1, the number may be omitted from the rule. The following selectors are therefore equivalent:

``` css
bar:nth-child(1n+0)   /* represents all bar elements, specificity (0,1,1) */
bar:nth-child(n+0)    /* same */
bar:nth-child(n)      /* same */
bar                   /* same but lower specificity (0,0,1) */
```

 If b=0, then every ath element is picked. In such a case, the +b (or -b) part may be omitted unless the a part is already omitted.

``` css
tr:nth-child(2n+0) /* represents every even row of an HTML table */
tr:nth-child(2n) /* same */
```

 Whitespace is permitted after the "`(`", before the "`)`", and on either side of the "`+`" or "`-`" that separates the an and b parts when both are present. Valid Examples with white space:

``` css
:nth-child( 3n + 1 )
:nth-child( +3n - 2 )
:nth-child( -n+ 6)
:nth-child( +6 )
```

 Invalid Examples with white space:

``` css
:nth-child(3 n)
:nth-child(+ 2n)
:nth-child(+ 2)
```

 If both a and b are equal to zero, the pseudo-class represents no element in the document tree.

The value a can be negative, but only the positive values of an+b, for n≥0, may represent an element in the document tree.

``` css
html|tr:nth-child(-n+6)  /* represents the 6 first rows of XHTML tables */
```

## <span>`:nth-last-child()` pseudo-class</span>

The `:nth-last-child(an+b)` pseudo-class notation represents an element that has an+b-1 siblings after it in the document tree, for any positive integer or zero value of n, and has a parent element. See `:nth-child()` pseudo-class for the syntax of its argument. It also accepts the ‘`even`’ and ‘`odd`’ values as arguments.

### <span>Examples:</span>

``` css
tr:nth-last-child(-n+2)    /* represents the two last rows of an HTML table */

foo:nth-last-child(odd)    /* represents all odd foo elements in their parent element,
counting from the last one */
```

## <span>`:nth-of-type()` pseudo-class</span>

The `:nth-of-type(an+b)` pseudo-class notation represents an element that has an+b-1 siblings with the same expanded element name before it in the document tree, for any zero or positive integer value of n, and has a parent element. See `:nth-child()` pseudo-class for the syntax of its argument. It also accepts the ‘`even`’ and ‘`odd`’ values.

This allows an author to alternate the position of floated images:

``` css
img:nth-of-type(2n+1) { float: right; }
img:nth-of-type(2n) { float: left; }
```

## <span>`:nth-last-of-type()` pseudo-class</span>

The `:nth-last-of-type(an+b)` pseudo-class notation represents an element that has an+b-1 siblings with the same expanded element name after it in the document tree, for any zero or positive integer value of n, and has a parent element. See `:nth-child()` pseudo-class for the syntax of its argument. It also accepts the ‘`even`’ and ‘`odd`’ values.

To represent all h2 children of an XHTML body except the first and last, one could use the following selector:

``` css
body > h2:nth-of-type(n+2):nth-last-of-type(n+2)
```

In this case, one could also use :not(), although the selector ends up being just as long:

``` css
body > h2:not(:first-of-type):not(:last-of-type)
```

## <span>`:first-child` pseudo-class</span>

Same as `:nth-child(1)`. The `:first-child` pseudo-class represents an element that is the first child of some other element.

The following selector represents a p element that is the first child of a div element:

``` css
div > p:first-child
```

This selector can represent the p inside the div of the following fragment:

``` html
<p> The last P before the note.</p>
<div class="note">
   <p> The first P inside the note.</p>
</div>
```

but cannot represent the second p in the following fragment:

``` html
<p> The last P before the note.</p>
<div class="note">
   <h2> Note </h2>
   <p> The first P inside the note.</p>
</div>
```

The following two selectors are usually equivalent:

``` css
* > a:first-child /* a is first child of any element */
a:first-child /* Same (assuming a is not the root element) */
```

## <span>`:last-child` pseudo-class</span>

Same as `:nth-last-child(1)`. The `:last-child` pseudo-class represents an element that is the last child of some other element.

The following selector represents a list item li that is the last child of an ordered list ol.

``` css
ol > li:last-child
```

## <span>`:first-of-type` pseudo-class</span>

Same as `:nth-of-type(1)`. The `:first-of-type` pseudo-class represents an element that is the first sibling of its type in the list of children of its parent element.

The following selector represents a definition title `dt` inside a definition list `dl`, this `dt` being the first of its type in the list of children of its parent element.

``` css
dl dt:first-of-type
```

It is a valid description for the first two `dt` elements in the following example but not for the third one:

``` html
<dl>
 <dt>gigogne</dt>
 <dd>
  <dl>
   <dt>fusée</dt>
   <dd>multistage rocket</dd>
   <dt>table</dt>
   <dd>nest of tables</dd>
  </dl>
 </dd>
</dl>
```

## <span>`:last-of-type` pseudo-class</span>

Same as `:nth-last-of-type(1)`. The `:last-of-type` pseudo-class represents an element that is the last sibling of its type in the list of children of its parent element.

The following selector represents the last data cell td of a table row `tr`.

``` css
tr > td:last-of-type
```

## <span>`:only-child` pseudo-class</span>

Represents an element that has a parent element and whose parent element has no other element children. Same as `:first-child:last-child` or `:nth-child(1):nth-last-child(1)`, but with a lower specificity.

## <span>`:only-of-type` pseudo-class</span>

Represents an element that has a parent element and whose parent element has no other element children with the same expanded element name. Same as `:first-of-type:last-of-type` or `:nth-of-type(1):nth-last-of-type(1)`, but with a lower specificity.

## <span>`:empty` pseudo-class</span>

The `:empty` pseudo-class represents an element that has no children at all. In terms of the document tree, only element nodes and content nodes (such as DOM [[DOM-LEVEL-3-CORE](http://www.w3.org/TR/2011/REC-css3-selectors-20110929/#DOM-LEVEL-3-CORE)] text nodes, CDATA nodes, and entity references) whose data has a non-zero length must be considered as affecting emptiness; comments, processing instructions, and other nodes must not affect whether an element is considered empty or not.

p:empty is a valid representation of the following fragment:

``` html
<p></p>
```

foo:empty is not a valid representation for the following fragments:

``` html
<foo>bar</foo>

<foo><bar>bla</bar></foo>

<foo>this is not <bar>:empty</bar></foo>
```