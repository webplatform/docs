---
title: Advanced selectors guide
notes:
  - 'Need to remove compatibility table.'
readiness: 'Ready to Use'
summary: 'This guide gives a detailed explanation of most of the advanced CSS selectors available.'
tags:
  - Guides
  - CSS
uri: 'guides/advanced selectors guide'

---
## Summary

This guide gives a detailed explanation of most of the advanced CSS selectors available.

## Introduction

In our [Using selectors](/tutorials/using_selectors) article, we introduced the most basic of CSS selectors: element, class, and id selectors. With these selectors you can accomplish a lot, but this certainly is not an exhaustive list of selectors — there are other selectors that allow you to select elements to style based on more specific criteria. In this article, most of the advanced CSS selectors are described.

Note: This article discusses *most* of the advanced selectors, because although most modern browsers support all the selectors listed in the [CSS3 selectors module](http://www.w3.org/TR/selectors/), new selectors are being added and modified all the time--keep checking the [CSS4 selectors draft](http://www.w3.org/TR/selectors4/) for updates. New selectors will be added to this article as they receive more widespread browser support.

You will see many of these selectors used throughout our articles as you read on. Don't worry if you don't understand them all immediately: keep referencing this article as needed.

## Universal selectors

Universal selectors select every element on a page. For example, the following rule says that every element on the page will display a solid 1 pixel black border:

``` css
* {
  border: 1px solid #000000;
}
```

## Attribute selectors

Attribute selectors allow you to select elements based on the attributes they contain. For example, you can select every `<img>` element with an `alt` attribute using the following selector:

``` css
img[alt] {
  border: 1px solid #000000;
}
```

 Note the square brackets in the example above.

Using the above selector, you could perhaps add a black border around any images that have an `alt` attribute, and style other images with a bright red border — this is a useful technique for accessibility testing.

### Selecting by attribute value

Attribute selectors instantly become more useful when you consider that you can select by *attribute value*, not just an attribute's name. The following rule selects all images with an `src` attribute value of `alert.gif`:

``` css
img[src="alert.gif"] {
  border: 1px solid #000000;
}
```

 Again this style is useful for debugging purposes. You can also use it to style important icons or links without requiring additional classes and IDs.

Note that this code is not supported by IE6 and below.

### Selecting based on substrings within the attribute value

This is where attribute selectors become even more useful. To begin, you can select and style our `<img src="alert.gif">` element using the following rule:

``` css
img[src^="alert"] {
  border: 1px solid #000000;
}
```

 The \^ character dictates that this selector affects `<img>` elements only if they contain the string `alert` at the start of the `src` attribute value.

You can also select a `<img src="alert.gif">` element using this rule:

``` css
img[src$="gif"] {
  border: 1px solid #000000;
}
```

 The \$ character dictates that this selector should select `<img>` elements only if they contain the string `gif` at the end of the `src` attribute value. This is really useful for styling links that point to specific types of resources, such as PDF files or word documents.

And finally, you can select a `<img src="alert.gif">` element like this:

``` css
img[src*="ert"] {
  border: 1px solid #000000;
}
```

 The \* character dictates that this selector should affect `<img>` elements only if they have the string `ert` anywhere within the `src` attribute value.

Note: These advanced selectors are not supported by IE8 and below.

### Selecting based on delimited items within the attribute value

If you have an element on a page with a number of classes applied to it, for example:

    <article class="featured archive english"></article>

You could select it using any of the following selectors:

``` css
article[class~="featured"]
article[class~="archive"]
article[class~="english"]
```

 The \~ character dictates that these selectors should select an `<article>` element whose `class` attribute value is a list of whitespace-separated values, but only if one of those values is the value given inside the quotes.

Next, take a look at an element on a page with an ID value in the form of hyphen-separated list:

    <article id="english-daily-feature"></article>

You can select it using the following selector:

``` css
article[id|="english"]
```

 The | character dictates that this selector should select an `<article>` element whose `id` attribute value is a list of hyphen-separated values, but only if the leftmost value is `english`.

Note: These selectors are not supported by IE8 and below.

## Child selector

You can use a child selector to select specific elements that are children of other specific elements. For example, the following rule will turn the text of `<strong>` elements that are children of `<h3>` elements blue, without affecting other `<strong>` elements:

``` css
h3 > strong {
  color: blue;
}
```

 Note that child selectors are not supported in IE6 or below.

Note also that the \> character is often referred to as a combinator in this context — it combines multiple elements together in one selector.

## Descendent selector

Descendent selectors are similar to child selectors, except that child selectors only select immediate descendants; descendent selectors select matching elements anywhere in the element hierarchy, not just direct descendants. Investigate what this means by examining the following HTML snippet:

``` html
<div>
  <p>hello</p>
  <article>
    <p>In this paragraph I will say goodbye</p>
  </article>
</div>
```

 In this snippet, the `<div>` element is the parent of all other elements. It has two children, a `<p>` and an `<article>`. The `<article>` element has a single child element: another `<p>`.

You could use a child selector to select just the `<p>` immediately inside the `<div>`, like so:

``` css
div > p {
 …
}
```

 If you instead use a descendent selector, as follows:

``` css
div p {
 …
}
```

 Then, both of the `<p>` elements are selected.

## Adjacent sibling selector

This selector allows you to select a specific element that comes directly after another specific element, on the same level in the element hierarchy. Review the following example:

``` html
<h2>My heading</h2>
<p>My first paragraph</p>
<p>My second paragraph</p>
<p>My third paragraph</p>
<p>My fourth paragraph</p>
<p>My fifth paragraph</p>
```

If you wanted to select just the `<p>` element that comes immediately after the `<h2>` element (and any other such `<p>` elements that might appear later in the document) you could use the following rule:

``` css
h2 + p {
 ...
}
```

 Note that the adjacent sibling selector is not supported in IE6 or below.

Note also that the + character is often referred to as a combinator in this context — it combines multiple elements together in one selector.

## General sibling selectors

The general sibling selector is very similar to the adjacent sibling selector, except that it allows you to select all siblings of the specified element type, not just the one immediate next to the element on the left side. The CSS syntax looks like this:

``` css
h2 ~ p {
 ...
}
```

 Returning to our previous example, this ruleset would select all five paragraph elements, not just the first one. It would also select the paragraph shown below:

``` html
<h2>My heading</h2>
<h3>My sub heading</h3>
<p>My paragraph</p>
```

 Note that the general sibling selector is not supported in IE8 or below.

Note also that the \~ character is often referred to as a combinator in this context — it combines multiple elements together in one selector.

## Pseudo-classes

Pseudo-classes are used to provide styles not for elements, but for various states of elements.

### Link and user action pseudo-classes

The most common pseudo-classes you will come across are those used to style link states (they are described in full usage in [Styling lists and links](http://docs.webplatform.org/wiki/Styling_lists_and_links)):

-   `:link` — the normal, default state of links, as displayed when the page first loads in a browser.
-   `:visited` — selects links that you have already visited in the browser you are currently using.
-   `:focus` — selects links that currently have the text indicator (location of cursor) within them.
-   `:hover` — selects links that the cursor is currently hovering over.
-   `:active` — selects links that are currently being clicked.

Note that the last three listed above (called "user action pseudo-classes" — the first two are the link pseudo-classes) can be used to style the states of any element. They are often used when styling a user interface. For example, you can set a different style of a form input field when it is tabbed into, or you might want an information box to appear only when the cursor hovers over a certain area of the screen.

Check out the following examples. The CSS rules below applies a link style to display blue links (which is the default link style in most browsers anyway). When hovered over, the default link underline disappears. To achieve the same effect when the link is focused via the keyboard, the `:hover ` rule is duplicated with the `:focus ` selector. When a link has already been visited, it turns gray. Finally, when a link is active, it is bold, as an extra clue to visitors that something significant is happening.

``` css
a:link {
 color: blue;
}

a:visited {
 color: gray;
}

a:hover, a:focus {
text-decoration: none;
}

a:active {
 font-weight: bold;
}
```

 Take care to specify these rules in the same order as they are shown in above, because otherwise they might not work as you expect. This is due to the way specificity causes later rules in the style sheet to override earlier rules. Specificity is covered in more detail in the article titled [Inheritance and cascade](/tutorials/inheritance_and_cascade).

As another example, the `:focus` pseudo-class is also useful as a usability aid in forms. For example, you can highlight the input field that has the active blinking cursor inside it with a rule like this:

``` css
input:focus  {
  border: 2px solid black;
  background color: lightgray;
}
```

### The negation (not) pseudo-class

The negation pseudo-class can be used to explicitly apply styles to elements that **are not** selected by a simple selector. For example, imagine that you want to apply some styling to a number of content blocks, all except one. The blocks could look like this:

``` html
<section id="abstract"> ... </section>
<section id="experiment"> ... </section>
<section id="tests"> ... </section>
<section id="results"> ... </section>
<section id="conclusion"> ... </section>
<section id="references"> ... </section>
```

 You can apply the styling to all sections except the references, with this rule:

``` css
#abstract, #experiment, #tests, #results, #conclusion {
  ...
}
```

 Or instead, you can use the negation selector, like this:

``` css
section:not(#references) {
  ...
}
```

 Which is much shorter and easy to read.

Note: The negation selector is not supported by IE8 and below.

### The language (lang) pseudo-class

The `:lang` pseudo-class selects elements whose languages have been set to the specified language using the `lang` attribute. For example, the following HTML element:

``` html
<p lang="en-US">A paragraph of American text, gee whiz!<p>
```

 Could be selected using the following:

``` css
p:lang(en-US) {
 ...
}
```

### The target pseudo-class

The target pseudo-class allows you to select an element if it is the **target** of the current page URL. This is really useful and allows for some cool effects, because it effectively allows you to set styles to be applied when links are clicked. For example:

``` html
<a href="#target">Click me</a>

<div id="target">Woot!</div>
```

 This is accomplished with a simple link followed by a `<div>` — the link references the `<div>` via its ID. The current URL only targets the `<div>` upon the link being clicked. To style the `<div>` only when the link is clicked, you could use the following rule:

``` css
div:target {
  ...
}
```

 To see a much more involved example of `:target` usage, read the article titled [CSS3 target-based interfaces](http://dev.opera.com/articles/view/css3-target-based-interfaces/) by Corey Mwamba.

### UI element state pseudo-classes

These pseudo-classes are all concerned with styling advanced states of UI elements. You'll most commonly use them to style HTML form elements, particularly when some of the new features of HTML5 forms are being used, such as built in validation. (See [HTML5 form additions] for more details.)

Imagine you are styling a basic form input with a `valid` attribute for validation:

``` html
<input type="text" required>
```

 You can style it only when the information entered into it is valid or invalid using these two rules:

``` css
input:valid {}
```

 and

``` css
input:invalid {}
```

 You can also style it depending on whether it is enabled (default) or disabled (using the `disabled` attribute), using this style:

``` css
input:enabled {}
```

 and this style:

``` css
input:disabled {}
```

 Finally, you can style a checkbox only when checked, like this:

``` css
input[type="checkbox"]:checked {}
```

### Structural pseudo-classes

Structural pseudo-classes are advanced selectors that enable you to target specific elements based on their position in the document hierarchy. These were introduced in CSS3, and they are built on selectors previously discussed, such as the adjacent sibling selector.

`:root` selects the root element of the document, which is usually the `<html>` element. For example, this rule:

``` css
html:root{ ... }
```

`:nth-child(n)` allows you to select a repeating pattern of elements inside an continuous set of like elements, such as several list items, or several paragraphs or articles next to one another. Review this example:

``` html
<ul>
  <li>First</li>
  <li>Second</li>
  <li>Third</li>
  <li>Fourth</li>
  <li>Fifth</li>
  <li>Sixth</li>
  <li>Seventh</li>
  <li>Eighth</li>
  <li>Ninth</li>
  <li>Tenth</li>
</ul>
```

`n` is set to the pattern we want to select. In this case, to select list items, use this code:

``` css
li:nth-child(n)
```

 To select just the odd or even list items, add this rule:

``` css
li:nth-child(odd)
li:nth-child(even)
```

 Or you can use this rule to accomplish the same result:

``` css
li:nth-child(2n+1)
li:nth-child(2n+0)
```

 Take a look at some other formula examples:

-   `li:nth-child(5)`: select the fifth adjacent list item.
-   `li:nth-child(4n+1)`: select every fourth list item, and then add 1 to each result. So numbers 5 and 9.
-   `li:nth-child(3n-2)`: select every third list item, and subtract 2 from each result. So numbers 1, 4 and 7.

You can also use `nth-last-child(n)`. This does the same thing as `nth-child(n)`, but it counts from the last element in the sequence, not the first element.

`nth-of-type(n)` and `nth-last-of-type(n)` accomplish almost exactly the same goals as `nth-child(n)` and `nth-last-child(n)`, but there is one important difference: the former two ignore any rogue elements interspersed with the repeated sequence of like elements because they select by type of element, not by child number. The latter selects by child number.

Here is another example:

``` html
<div>
  1. <article class="abstract"> ... </article>
  2. <article class="abstract"> ... </article>
  3. <article class="abstract"> ... </article>
  4. <article class="abstract"> ... </article>
  5. <article class="abstract"> ... </article>
  6. <blockquote><p> ... </p></blockquote>
  7. <article class="abstract"> ... </article>
  8. <article class="abstract"> ... </article>
  9. <article class="abstract"> ... </article>
</div>
```

 In this example we've got a `<element>` with eight child `<article>` elements, and a single `<blockquote>` element in the middle of them: this is child number six. There are a total of nine child elements.

If you use `article:nth-child(2n+0)` as the selector, to select all the even-numbered children of the `<div>`, you'd select only the `<article>`s in positions 2, 4 and 8: the `<blockquote>` (position number six) is not selected because it is not an `<article>`.

If you use `article:nth-of-type(2n+0)` as the selector, you would select the `<article>`s in positions 2, 4, 7 and 9: this occurs because it selects by the type of element, not the child position. Therefore in this case, the `<blockquote>` is completely ignored and the even numbered `<article>`s are selected. Yes, two of them are odd numbered according to my original numbering scheme because in reality the `<blockquote>` exists and offsets their position, but `article:nth-of-type(2n+0)` ignores the `<blockquote>`, effectively counting positions 7 and 9 as 6 and 8.

Next, check out the `:first-child` and `:last-child` selectors — these pseudo-classes select only the first or last instance of an element that is the first or last child element of its parent. So, considering the above example again, we could use the following to select - respectively - the first and last `<article>` element:

``` css
article:first-child { ... }

article:last-child { ... }
```

`blockquote:first-child` would select nothing, because the first child is not a `<blockquote>`.

`first-of-type` and `last-of-type` again work in a very similar way, but they select based on the type of element, not the position of child it is. So `article:first-of-type` selects exactly the same `<article>` element as `article:first-child`, but `blockquote:first-of-type` selects the single `<blockquote>` in the example, because it is the first of its type, even though it is the sixth child.

There are a few others to consider:

-   `only-child`: Selects an element only if it is the only child of its parent. The selector `article:only-child` wouldn't select anything in our example above, because there is more than one `<article>` child.
-   `only-of-type`: Selects an element only if it is the only sibling of its type inside the parent element. So `blockquote:only-of-type` would select the `<blockquote>` in the above example because it is the only one of its type that exists.
-   `empty`: selects an element only if it has no children whatsoever (including text nodes). For example `div:empty` would select `<div></div>`, but not `<div>1</div>` or `<div><p>Hi!</p></div>`

## Pseudo-elements

Pseudo elements differ from pseudo-classes in that they don't select states of elements; they select parts of an element.

### :first-letter

You can select the first letter inside a given element using the following rule:

``` css
p:first-letter {
  font-weight: bold;
  font-size: 300%
  background-color: red;
}
```

 The first letter of every paragraph will now be bold, 300% bigger than the rest of the paragraph, and have a red background. This is a good start towards creating a decent drop cap effect.

### :first-line

To make the first line of every paragraph bold, you can use the following rule:

``` css
p:first-line {
  font-weight: bold;
}
```

### Generated content using :before and :after

You can use the `:before` and `:after` pseudo-elements to specify that content should be inserted before and after the selected element. You then specify the content that you want to insert or generate. For example, you can use the following rule to insert a decorative image after every link on the page:

``` css
a:after {
  content: " " url(flower.gif);
}
```

 You can also use the `attr()` function to insert the values of attributes of the elements after the element. For example, you could insert the target of every link in your document in brackets after each one using the following:

``` css
a:after {
  content: "" "(" attr(href) ")";
}
```

 This is a great technique to use in a print style sheet, where it is important to display the URLs in the document rather than have them hidden inside text links (which are useless on a printed page).

You can also insert incremented numerical values after repeating elements (such as bullets or paragraphs) using the `counter()` function. This is explained in much more detail in the article titled [[Automatic numbering with CSS counters](http://dev.opera.com/articles/view/automatic-numbering-with-css-counters/)] by David Storey.

These selectors are not supported in IE 7 or below. Also note that you should not insert important information with CSS, because that content will be unavailable to assistive technologies. It will also be unavailable if a visitor chooses not to use the style sheet. The golden rule is that CSS rules are for styling; HTML is for displaying important content.

### CSS3 pseudo-element double colon syntax

Please note that the new CSS3 way of writing pseudo-elements is to use a double colon, such as `a::after { … }`, to set them apart from pseudo-classes. You may see this sometimes in CSS. CSS3 however also still allows for single colon pseudo-elements, for the sake of backwards compatibility. For the immediate future, it is recommended to continue using the single colon syntax.
