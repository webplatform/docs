---
title: counter-increment
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/5841845'
  - 'http://gist.github.com/5841870'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`none`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': ''
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
readiness: 'Ready to Use'
summary: 'The counter-increment property accepts one or more names of counters (identifiers), each one optionally followed by an integer which specifies the value by which the counter should be incremented (e.g. if the value is 2, the counter increases by 2 each time it is invoked).'
tags:
  - CSS
  - Properties
uri: css/properties/counter-increment

---
## <span>Summary</span>

The counter-increment property accepts one or more names of counters (identifiers), each one optionally followed by an integer which specifies the value by which the counter should be incremented (e.g. if the value is 2, the counter increases by 2 each time it is invoked).

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `none`

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

## <span>Syntax</span>

-   `counter-increment: identifier`
-   `counter-increment: integer`

## <span>Values</span>

identifier
:   The name of the counter. The counter can then be invoked by using **counter(\<identifier\>)**.

integer
:   An integer that indicates by how much the counter is

incremented for every occurrence of the element. Zero and negative integers are allowed. If no value is specified, the value defaults to 1.

## <span>Examples</span>

This example uses **counter-increment** and the **content** properties to prepend headers with an outline-esque, identifier, similar to an ordered list. (Note that the numbering does not reset between the two headers: this can be handled with [**counter-reset**](/css/properties/counter-reset).)

``` css
/*
 * Using the CSS 'counter-increment' property.
 */

h1 {
    counter-increment: header;
}

h1:before {
    content: counter(header) ". ";
}

h2 {
    counter-increment: subheader;
}

h2:before {
    content: counter(header) "." counter(subheader) ". ";
}
```

[View live example](http://code.webplatform.org/gist/5841845)

This example shows how to specify an integer in the **counter-increment** property and allow the CSS to increment the counter by values besides 1.

``` css
/*
 * Using the CSS 'counter-increment' property with a non-default increment JavaScript.
 */

/* In this example, we specify both an identifier and an integer -- the integer is the number
 * which the counter is increased by every time it is used.
 */
h1 {
    counter-increment: header 3;
}

/* Using the pseudo-element `:after`, we place the counter after each valid `h1` tag. */
h1:after {
    content: counter(header) ". ";
}
```

[View live example](http://code.webplatform.org/gist/5841870)

## <span>Usage</span>

     It is important to note that counter-increment can handle multiple counters and non-positive integers, though best practices often dictates that counters should be defined separately.

## <span>Notes</span>

### <span>Remarks</span>

The **counter-increment** attribute can contain a list of one or more counters, each one optionally followed by an integer. The integer represents the amount that the counter is incremented after each occurrence of an element. This property is used to generate numbered content for each occurrence of an element. The counter need not be defined before it is incremented. To reset a counter value, use the [**counter-reset**](/css/properties/counter-reset) attribute. An element that is not displayed ([**display**](/css/properties/display) attribute set to 'none') and pseudo-elements that do not generate content ([**content**](/css/properties/content) attribute set to 'normal') cannot increment or reset a counter. This property requires Windows Internet Explorer to be in IE8 Standards mode rendering.

### <span>Syntax</span>

`counter-increment: '[  <identifier>   <integer>  ]'+`

### <span>Standards information</span>

-   [CSS 2.1](http://go.microsoft.com/fwlink/p/?linkid=203757), Section 12.4

## <span>See also</span>

### <span>Related articles</span>

#### <span>Generated and Replaced Content</span>

-   [Generated and Replaced Content](/css/generated_and_replaced_content)

-   [content](/css/properties/content)

-   **counter-increment**

-   [counter-reset](/css/properties/counter-reset)

-   [list-style-image](/css/properties/list-style-image)

-   [list-style-type](/css/properties/list-style-type)

-   [object-fit](/css/properties/object-fit)

### <span>Related pages (MSDN)</span>

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `runtimeStyle`
-   `style`
-   `counter-reset`
