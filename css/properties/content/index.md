---
title: 'content'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/6948299'
  - 'http://gist.github.com/6948575'
  - 'http://gist.github.com/6948854'
  - 'http://gist.github.com/6949103'
  - 'http://gist.github.com/6949289'
compatibility:
  feature: content
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`normal`'
  'Applies to': "pseudo-elements\_:before and\_:after"
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'On elements, always computers to normal.'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`content`'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: "The content property is used to display content in the pseudo-elements\_::before and\_::after."
tags:
  - CSS_Properties
  - CSS
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - before
uri: css/properties/content

---
## Summary

The content property is used to display content in the pseudo-elements ::before and ::after.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `normal`

Applies to
:   pseudo-elements :before and :after

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   On elements, always computers to normal.

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:   `content`

## Syntax

-   `content: attr`
-   `content: close-quote`
-   `content: counter`
-   `content: no-close-quote`
-   `content: no-open-quote`
-   `content: none`
-   `content: normal`
-   `content: open-quote`
-   `content: string`
-   `content: uri`

## Values

none
:   Pseudo element is not generated.

normal
:   Equivalent to "none" for :before and :after pseudo-elements, which are the only places the content property currently applies.

string
:   Text content, in either double quotation marks (") or single quotation marks (').

Double quotation marks cannot occur inside other double quotation marks, unless they are preceded by a backslash (\\) escape character. For example, the string `"\""` is interpreted as containing one double quotation character.

It is possible to break strings over several lines, for esthetic or other reasons, by use of the backslash as a continuation character; however, the newline character itself is ignored.

Newlines can be used by writing the `\A` escape sequence in any of the strings after the **content** property. The generated line break is displayed in accordance with the value of the [**white-space**](/css/properties/white-space) attribute.

The backslash is also used to generate escape characters that cannot be represented in the current character encoding. In this case, the backslash is followed by at most six hexadecimal digits (from the range 0–9 and A–F) to indicate the Unicode character with that number.

uri
:   This is the url of an external resource, such as an image. If the user agent cannot display the resource it must either leave it out as if it were not specified or display some indication that the resource cannot be displayed.

counter
:   Counters may be specified with two different functions: 'counter()' or 'counters()'. 'counter()' has two forms: 'counter(name)' or 'counter(name, style)'. The generated text is the value of the innermost counter of the given name in scope at this pseudo-element; it is formatted in the indicated style ('decimal' by default). 'counters()' also has two forms: 'counters(name, string)' or 'counters(name, string, style)'. The generated text is the value of all counters with the given name in scope at this pseudo-element, from outermost to innermost separated by the specified string.

The counters are rendered in the indicated style ('decimal' by default). The name must not be 'none', 'inherit' or 'initial'. Such a name causes the declaration to be ignored.

open-quote
:   Sets the content to be the appropriate string from the quotes property.

close-quote
:   Sets the content to be the appropriate string from the quotes property.

no-open-quote
:   If set, removes the opening quote from the content.

no-close-quote
:   If set, removes the closing quote from the content.

attr
:   Value of an attribute of the subject of the selector. If attribute is not set on the subject an empty string will be returned. It is used as a function with the element name as the argument: 'attr( element-name )'

## Examples

The following example generates braces before and after all the **h1** elements on a page.

``` css
h1:before {
    content: "{ ";
}
h1:after {
    content: " }";
}
```

[View live example](http://gist.github.com/6948299)

Using attr( element-name ) to display text from an attribute. The following example adds a box displaying the value of the data-badge attribute for a button element.

``` css
button[data-badge] {
    /* the badge is going to be positioned absolute in the
     * button. Therefore the button needs a relative position */
    position: relative;
}

button[data-badge]:after {
    /* use the data-badge attribute as value for the pseudo element */
    content: attr( data-badge );

    /* give the badge some nice styling */
    background: tomato;
    display: block;
    border-radius: 4px;
    position: absolute;
    right: -4px;
    top: -4px;
    padding: 1px 4px;
}
```

[View live example](http://gist.github.com/6948575)

Using the uri data-type the webplatform favicon is appended to all elements with the webplatform class.

``` css
.webplatform:before {
    content: url('http://docs.webplatform.org/favicon.ico');
}
```

[View live example](http://gist.github.com/6948854)

Uses the counter data-type to show a automatic numbering for all h2 elements on the page. More information is available on the [**counter-increment**](/css/properties/counter-increment) property page.

``` css
h2 {
/*  increment header counter per h2 element */
    counter-increment: header;
}

h2:before {
/*  show header counter before each h2 element */
    content: counter(header) ". ";
}
```

[View live example](http://gist.github.com/6949103)

Uses the open-quote and close-quote data-type to add quoting around each blockquote element on the page.

``` css
blockquote:before {
    content: open-quote;
}

blockquote:after {
    content: close-quote;
}
```

[View live example](http://gist.github.com/6949289)

## Notes

-   CSS2.1 uses a single colon, and most browsers still support this. CSS3 introduces the use of double colons to avoid confusion with pseudo-classes.

## Related specifications

[Generated content, automatic numbering and lists](http://www.w3.org/TR/CSS21/generate.html#propdef-content)
:   Recommendation

## See also

### Related articles

#### Generated and Replaced Content

-   [Generated and Replaced Content](/css/generated_and_replaced_content)

-   **content**

-   [counter-increment](/css/properties/counter-increment)

-   [counter-reset](/css/properties/counter-reset)

-   [list-style-image](/css/properties/list-style-image)

-   [list-style-type](/css/properties/list-style-type)

-   [object-fit](/css/properties/object-fit)

#### Multi-Column

-   [break-after](/css/properties/break-after)

-   [break-before](/css/properties/break-before)

-   [break-inside](/css/properties/break-inside)

-   [column-count](/css/properties/column-count)

-   [column-gap](/css/properties/column-gap)

-   [column-rule](/css/properties/column-rule)

-   [column-rule-color](/css/properties/column-rule-color)

-   [column-rule-style](/css/properties/column-rule-style)

-   [column-rule-width](/css/properties/column-rule-width)

-   [column-span](/css/properties/column-span)

-   [column-width](/css/properties/column-width)

-   **content**

### Other articles

-   [counter-increment](/css/properties/counter-increment)
-   [counter-reset](/css/properties/counter-reset)
-   [before](/Special:FormEdit/Method/before?redlink=1)
-   [after](/after)

### External resources

-   CSS-Tricks: CSS Content [[1]](http://css-tricks.com/css-content/)
