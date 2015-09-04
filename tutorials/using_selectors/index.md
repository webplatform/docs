---
title: using selectors
tags:
  - Tutorials
  - CSS
readiness: 'Ready to Use'
summary: 'This guide looks at CSS selectors — the mechanism you use to select which element receives styles — in detail, the different types of selectors available, and how different kinds of selectors have different priorities.'
uri: 'tutorials/using selectors'

---
# Using selectors

## Summary

This guide looks at CSS selectors — the mechanism you use to select which element receives styles — in detail, the different types of selectors available, and how different kinds of selectors have different priorities.

## Information: Selectors

CSS has its own terminology to describe the CSS language. In a previous tutorial, you created a line in your stylesheet like this:

``` {.css}
strong {
  color: red;
}
```

 In CSS terminology, this entire code section is a *rule*. The rule starts with `strong`, which is a *selector*. It selects which elements in the DOM the rule applies to.

-   The part inside the braces is the *declaration*.
-   The keyword `color` is a *property*, and `red` is a *value*.
-   The semicolon after the property-value pair separates it from other property-value pairs in the same declaration.

This guide refers to a selector like `strong` as a *tag* selector; you will also see it commonly referred to as an *element* selector. The CSS Specification refers to it as a *type* selector.

In addition to tag names, you can use attribute values in selectors. This allows your rules to be more specific. Two attributes, [class](/html/attributes/class) and [id](/html/attributes/id), have special status for CSS.

### Class selectors

Use the `class` attribute in an element to assign the element to a named class. It is up to you what name you choose for the class. Multiple elements in a document can have the same class value.

In your style sheet, type a dot (period) before the class name when you use it in a selector.

### ID selectors

Use the `id` attribute in an element to assign an ID to the element. It is up to you what name you choose for the ID. The ID name must be unique in the document.

In your stylesheet, type a number sign (hash) before the ID when you use it in a selector.

### Class and ID selector example

This HTML tag has both a `class` attribute and an `id` attribute:

``` {.html}
<p class="key" id="principal">
```

 The **id** value `principal` must be unique in the document, but other tags in the document can have the same `key` **class** name.

In a CSS style sheet, this rule makes all the elements with class `key` green. (They might not all be `<p>` elements.)

``` {.css}
.key {
  color: green;
}
```

 This rule makes the one element with the **id** `principal` bold:

``` {.css}
#principal {
  font-weight: bold;
}
```

 If more than one rule applies to an element and specifies the same property, then CSS gives priority to the rule that has the more specific selector. An ID selector is more specific than a class selector, which in turn is more specific than a tag selector.

### Combining selectors

You can also combine selectors, making a more specific selector.

For example, the selector `.key` selects all elements that have the class name `key`. The selector `p.key` selects only `<p>` elements that have the class name `key`.

You are not restricted to the two special attributes, `class` and `id`. You can specify other attributes by using brackets. For example, the selector `[type='button']` selects all elements that have a `type` attribute with the value `button`.

If the style sheet has conflicting rules and they are equally specific, then CSS gives priority to the rule that is later in the style sheet.

When you have a problem with conflicting rules, try to resolve it by making one of the rules more specific, so that it has priority. If you cannot do that, try moving one of the rules nearer to the end of the style sheet so that it has priority.

### Pseudo-class selectors

A CSS [pseudo-class](/css/selectors/pseudo-classes) is a keyword added to selectors that specifies a special state of the element to be selected. For example, [:hover](/css/selectors/pseudo-classes/:hover) will apply a style when the user hovers over the element specified by the selector.

Pseudo-classes, together with pseudo-elements, let you apply a style to an element not only in relation to the content of the document tree, but also in relation to external factors like the history of the navigator ([visited](/css/selectors/pseudo-classes/:visited), for example), the status of its content (like [:checked](/css/selectors/pseudo-classes/:checked) on some form elements), or the position of the mouse (like [:hover](/css/selectors/pseudo-classes/:hover), which lets you know if the mouse is over an element or not). For a complete list of selectors, see [css/selectors](/css/selectors).

``` {.css}
selector:pseudo-class {
  property: value;
}
```

## Information: Selectors based on relationships

CSS has some ways to select elements based on the relationships between elements. You can use these to make selectors that are more specific.

||
|**Selector**|**Selects**|
|`A E`|Any E element that is a *descendant* of an A element (that is: a child, or a child of a child, *etc*.)|
|`A > E`|Any E element that is a child of an A element|
|`E:first-child`|Any E element that is the first child of its parent|
|`B + E`|Any E element that is the next *sibling* of a B element (that is: the next child of the same parent)|

You can combine these to express complex relationships. You can also use the symbol `*` (asterisk) to mean "any element".

#### Example of selectors based on relationships

This HTML table has an `id` attribute, but its rows and cells do not have individual identifiers:

``` {.html}
<table id="data-table-1">
…
<tr>
<td>Prefix</td>
<td>0001</td>
<td>default</td>
</tr>
…
```

 The following rules make the first cell in each row bold, and the second cell in each row monospaced. They only affect one specific table in the document, the one with the id `<data-table-1>`:

``` {.css}
#data-table-1 td:first-child {font-weight: bold;}
#data-table-1 td:first-child + td {font-family: monospace;}
```

 The result looks like:

<table>
<col width="100%" />
<tbody>
<tr class="odd">
<td align="left"><dl>
<dt><strong>Prefix</strong></dt>
<dd><code>0001</code>
</dd>
</dl></td>
</tr>
</tbody>
</table>

### Increasing specificity

In the usual way, if you make a selector more specific, then you increase its priority.

If you use these techniques, you avoid the need to specify `class` or `id` attributes on so many tags in your document. Instead, CSS does the work.

In large designs where speed is important, you can make your style sheets more efficient by avoiding complex rules that depend on relationships between elements.

## Action: Using class and ID selectors

1.  Create an HTML page with the following code:

    ``` {.html}
    <!doctype html>
     <html>
       <head>
       <meta charset="UTF-8">
       <title>Sample document</title>
       <link rel="stylesheet" href="style1.css">
       </head>
       <body>
         <p id="first">
           <strong class="carrot">C</strong>ascading
           <strong class="spinach">S</strong>tyle
           <strong class="spinach">S</strong>heets
         </p>
         <p id="second">
               <strong>C</strong>ascading
               <strong>S</strong>tyle
               <strong>S</strong>heets
             </p>
       </body>
     </html>
    ```

2.  Now edit your CSS file. Replace the entire contents with:

    ``` {.css}
    strong { color: red; }
     .carrot { color: orange; }
     .spinach { color: green; }
     #first { font-style: italic; }
    ```

3.  Save the files and refresh your browser to see the result:

![usingclassandid result.jpg](/assets/public/2/22/usingclassandid_result.jpg)

You can try rearranging the lines in your CSS file to show that the order has no effect. The class selectors `.carrot` and `.spinach` have priority over the tag selector `strong`. The ID selector `#first` has priority over the class and tag selectors.

### Exercise questions

-   Without changing the HTML file, add a single rule to your CSS file that leaves the initial letters the same color as they are now, but changes all the other text in the second paragraph to blue.
-   Change the rule you just added (without changing anything else), to set the first paragraph to blue.

## Action: Using pseudo-classes selectors

1.  Create an HTML page with the following code:

    ``` {.html}
    <!doctype html>
     <html>
       <head>
       <meta charset="UTF-8">
       <title>Sample document</title>
       <link rel="stylesheet" href="style1.css">
       </head>
       <body>
         <p>Go to our <a class="homepage" href="http://www.example.com/" title="Home page">Home page</a>.</p>
       </body>
     </html>
    ```

2.  Now edit your CSS file. Replace the entire contents with:

    ``` {.css}
    a.homepage:link, a.homepage:visited {
       padding: 1px 10px 1px 10px;
       color: #fff;
       background: #666;
       border-radius: 3px;
       border: 1px outset rgba(50,50,50,.5);
       font-family: georgia, serif;
       font-size: 14px;
       font-style: italic;
       text-decoration: none;
     }

     a.homepage:hover, a.homepage:focus, a.homepage:active {
       background-color: #333;
     }
    ```

3.  Save the files and refresh your browser to see the result (hover the mouse over the link to see the effect):

    ![pseudoclassselector result.jpg](/assets/public/8/84/pseudoclassselector_result.jpg)

    The link turns to dark grey.

## Action: Using selectors based on relationships and pseudo-classes

With selectors based on relationships and pseudo-classes you can create complex cascade algorithms. This is a common technique used, for example, in order to create **pure CSS drop down menus** (that is only CSS, without using JavaScript). The essence of this technique involves creating a rule like this:

``` {.css}
div.menu-bar ul ul {
  display: none;
}

div.menu-bar li:hover > ul {
  display: block;
}
```

 to be applied to an HTML structure like the following:

``` {.html}
<div class="menu-bar">
  <ul>
    <li>
      <a href="example.html">Menu</a>
      <ul>
        <li>
          <a href="example.html">Link</a>
        </li>
        <li>
          <a class="menu-nav" href="example.html">Submenu</a>
          <ul>
            <li>
              <a class="menu-nav" href="example.html">Submenu</a>
              <ul>
                <li><a href="example.html">Link</a></li>
                <li><a href="example.html">Link</a></li>
                <li><a href="example.html">Link</a></li>
                <li><a href="example.html">Link</a></li>
              </ul>
            </li>
            <li><a href="example.html">Link</a></li>
          </ul>
        </li>
      </ul>
    </li>
  </ul>
</div>
```

 In this way, CSS selectors can be used to create visual effects previously possible only with procedural languages like JavaScript.

## Conclusion

In this tutorial we examined various types of CSS selectors, how to use them to achieve different styling effects, and explored ways to affect the cascading order (priority) of CSS rules. For more information, see the other CSS tutorials in this section.

## Attribution

*This article contains content originally from external sources, including ones licensed under the CC-BY-SA license.* [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)

Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/en-US/docs/CSS/Getting_Started/Selectors)

