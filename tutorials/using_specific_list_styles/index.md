---
title: using specific list styles
tags:
  - Tutorials
  - CSS
readiness: 'Ready to Use'
summary: 'This article shows the basics of using list-specific CSS to control things like bullet appearance.'
uri: 'tutorials/using specific list styles'

---
# Using specific list styles

## Summary

This article shows the basics of using list-specific CSS to control things like bullet appearance.

## Information: Lists

You may recall from previous articles that you can add content before any element to display it as a list item. However, CSS provides special properties that are designed for lists, and it is usually more convenient to use these properties whenever you can.

To specify the style for a list, use the [list-style](/css/properties/list-style) property to specify the type of marker. The selector in your CSS rule can either select the list item elements `li`, or it can select the parent list element `ul` so that its list elements inherit the style.

### Unordered lists

In an *unordered* list, each list item is marked in the same way. CSS has three types of bullet markers: `disc`, `circle`, and `square`. Alternatively, you can specify the URL of an image file for the bullet icon.

These rules specify different markers for different classes of list items:

``` {.css}
li.open {list-style: circle;}
li.closed {list-style: disc;}
```

 When these classes are used in a list, they distinguish between open and closed items (for example, in a to-do list):

``` {.html}
 <ul>
   <li class="open">Lorem ipsum</li>
   <li class="closed">Dolor sit</li>
   <li class="closed">Amet consectetuer</li>
   <li class="open">Magna aliquot</li>
   <li class="closed">Autem vellum</li>
 </ul>
```

 The result might look like this:

![csslists1.png](/assets/public/e/e1/csslists1.png)

*Figure 1. Open and closed (circle and disc) list item bullets.*

You can also use [:nth-child](/css/selectors/pseudo-classes/Structural_pseudo-classes#:nth-child.28.29_pseudo-class) pseudo-class with the same result.

### Ordered lists

In an *ordered* list, each list item is marked differently to show its position in the sequence.

Again, use the [list-style](/css/properties/list-style) property to specify the type of marker: `decimal`, `lower-roman`, `upper-roman`, `lower-latin`, or `upper-latin`.

This rule specifies that in `ol` elements with the class `info`, the items are identified with capital letters.

``` {.css}
ol.info {list-style: upper-latin;}
```

 The `li` elements in the list inherit this style:

``` {.html}
<ol class="info">
   <li>Lorem ipsum</li>
   <li>Dolor sit</li>
   <li>Amet consectetuer</li>
   <li>Magna aliquot</li>
   <li>Autem vellum</li>
 </ol>
```

 And that result might look like this:

![csslists2.png](/assets/public/2/2f/csslists2.png)

*Figure 2. Ordered list items marked with capital letters.*

The `list-style` property is a shorthand property. In complex style sheets, you might prefer to use separate properties to set separate values. For links to these separate properties, and to learn more details about how CSS specifies lists, see [list-style](/css/properties/list-style).

Browsers differ in the way they implement the styles for lists. Do not expect your style sheet to provide identical results in all browsers.

### Counters

**Note:Â ** Some browsers do not support counters. The [CSSÂ contents and browser compatibility](http://www.quirksmode.org/css/contents.html) page on the [Quirks Mode](http://www.quirksmode.org/) site contains a detailed chart of browser compatibility for this and other CSS features. You can also find useful information about browser compatibility at the extensive [Can I Use](http://caniuse.com) site.

You can use counters to number any elements, not just list items. For example, in some documents you might want to number headings or paragraphs.

To specify numbering, you can add a *counter* with a name that you specify.

In some element before the counting is to start, reset the counter with the property `counter-reset` and the name of your counter. The parent of the elements you are counting is a good place to do this, but you can use any element that comes before the list items.

In each element where the counter should increment, use the property `counter-increment` and the name of your counter. Normally the element that displays the counter also increments it.

To display your counter, add `:before` or `:after` to the selector and use the `content` property to position the counter with the element. In the value of the `content` property, specify `counter()` with the name of your counter. Optionally specify a type. The types are the same as in the **Ordered lists** section above.

For example, this rule resets a counter called "mynum" when an `h3` with a class of `numbered` is encountered, preparing the paragraphs following the `h3` to be numbered.

``` {.css}
h3.numbered {counter-reset: mynum;}
```

 This rule displays and increments the counter for every subsequent `p` element with the class `numbered`.

``` {.css}
p.numbered:before {
   content: counter(mynum) ": ";
   counter-increment: mynum;
   font-weight: bold;
}
```

 So, for this HTML:

``` {.html}
<h3 class="numbered">This is an H3</h3>
<p class="numbered">This is a paragraph.</p>
<p class="numbered">This is a paragraph.</p>
<p class="numbered">This is a paragraph.</p>
```

 the result looks like this:

![csslists3.png](/assets/public/a/a0/csslists3.png)

*Figure 3. Numbered paragraphs using the `counter` property.*

You cannot use counters unless you are sure that everyone who reads your document has a browser that supports them. If you are able to use counters, they have the advantage that you can style the counters separately from the list items. In the example above, the counters are bold but the list items are not.

You can also use counters in more complex waysâ€”for example, to number sections, headings, subheadings and paragraphs in formal documents. For details, see [Automatic counters and numbering](http://www.w3.org/TR/CSS21/generate.html#counters) in the CSS Specification.

## Action: Styled lists

1.  Make a new HTML document, and name it `doc2.html`. Copy the code below and paste it into the document:

    ``` {.html}
     <!DOCTYPE html>
     <html>
       <head>
         <meta charset="UTF-8">
         <title>Sample document 2</title>
         <link rel="stylesheet" href="style2.css">
       </head>
       <body>
     Â
         <h3 id="oceans">The oceans</h3>
         <ul>
           <li>Arctic</li>
           <li>Atlantic</li>
           <li>Pacific</li>
           <li>Indian</li>
           <li>Southern</li>
         </ul>
     Â
         <h3 class="numbered">Numbered paragraphs</h3>
         <p class="numbered">Lorem ipsum</p>
         <p class="numbered">Dolor sit</p>
         <p class="numbered">Amet consectetuer</p>
         <p class="numbered">Magna aliquot</p>
         <p class="numbered">Autem vellum</p>
     Â
       </body>
     </html>
    ```

2.  Make a new style sheet, and name it `style2.css`. Copy the CSS below and paste it into the style sheet:

    ``` {.css}
    /* numbered paragraphs */
     h3.numbered {counter-reset: mynum;}
     Â
     p.numbered:before {
       content: counter(mynum) ": ";
       counter-increment: mynum;
       font-weight: bold;
     }
    ```

    If desired, you can edit the layout and comments.

3.  Open the document in your browser. If your browser supports counters, you see something like the example below. If your browser does not support counters, then you will not see the numbers (and it is likely that even the colons will not display):

    ![csslists4.png](/assets/public/7/78/csslists4.png)

    *Figure 4. Unordered list items and numbered paragraphs.*

-   Add a rule to your stylesheet to number the oceans using Roman numerals from i to v:
-   Change your stylesheet to identify the headings with capital letters in parentheses.

## Attribution

*This article contains content originally from external sources, including ones licensed under the CC-BY-SA license.* [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)

Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/en-US/docs/CSS/Getting_Started/Lists)

