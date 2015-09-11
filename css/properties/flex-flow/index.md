---
title: flex-flow
code_samples:
  - 'http://gist.github.com/4740728'
  - 'http://gist.github.com/5506026'
notes:
  - 'Add description and compatibility.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`See individual properties.`'
  'Applies to': 'flex containers'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'See individual properties.'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`flexFlow`'
readiness: 'In Progress'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The flex-flow CSS property defines the flex container''s main and cross axis. It is a shorthand property for the flex-direction and flex-wrap properties.'
tags:
  - CSS
  - Properties
  - Flexbox
uri: css/properties/flex-flow

---
## <span>Summary</span>

The flex-flow CSS property defines the flex container's main and cross axis. It is a shorthand property for the flex-direction and flex-wrap properties.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `See individual properties.`

Applies to
:   flex containers

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   See individual properties.

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `flexFlow`

## <span>Syntax</span>

-   `flex-flow: <flex-direction> <flex-wrap>`

## <span>Values</span>

\<flex-direction\> \<flex-wrap\>
:   The shorthand value includes the values of the following properties:

-   [flex-direction](/css/properties/flex-direction)
-   [flex-wrap](/css/properties/flex-wrap)

## <span>Examples</span>

Displaying children in a row wrapping to the next line.

``` css
.list {
  display: flex;
  flex-flow: row wrap;
}

.list div {
  flex: 1;
}
```

[View live example](http://code.webplatform.org/gist/4740728)

The Holy Grail Layout example.

``` css
flex-flow: row;
```

[View live example](http://code.webplatform.org/gist/5506026)

## <span>Related specifications</span>

[CSS Flexible Box Layout Module](http://www.w3.org/TR/css3-flexbox/#flex-flow-property)
:   Candidate Recommendation

## <span>See also</span>

### <span>Related articles</span>

#### <span>Flexbox</span>

-   [align-content](/css/properties/align-content)

-   [align-items](/css/properties/align-items)

-   [align-self](/css/properties/align-self)

-   [break-before](/css/properties/break-before)

-   [flex](/css/properties/flex)

-   [flex-basis](/css/properties/flex-basis)

-   [flex-direction](/css/properties/flex-direction)

-   **flex-flow**

-   [flex-grow](/css/properties/flex-grow)

-   [flex-shrink](/css/properties/flex-shrink)

-   [flex-wrap](/css/properties/flex-wrap)

-   [justify-content](/css/properties/justify-content)

### <span>External resources</span>

Also, check out the following live demo sites:

-   [Flexbox Playground](http://demo.agektmr.com/flexbox/)
-   [Flexy Boxes](http://the-echoplex.net/flexyboxes)
