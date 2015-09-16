---
title: SVGException
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Unreviewed MSDN import'
readiness: 'Not Ready'
relationships:
  subclass_of:
    predicate: 'Inherits from '
    value: SVGElement
    href: /svg/objects/SVGElement
tags:
  - API
  - Objects
  - DOM
uri: svg/objects/SVGException

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Inherits from [SVGElement](/svg/objects/SVGElement)[SVGElement](/svg/objects/SVGElement)

## Properties

*No properties.*

## Methods

*No methods.*

## Events

*No events.*

## Inherited from SVGElement

### Properties

*No properties.*

### Methods

*No methods.*

### Events

*No events.*

**Needs Examples**: This section should include examples.

## Notes

### Remarks

**Note:** In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

The following constants exist in group **SVGException** code:

-   **SVGWrongTypeError**

is raised when an object of the wrong type is passed to an operation.

**Note:** No operation is defined to raise an **SVGException** exception with this code in the SVG 1.1 Second Edition specification. The constant is defined for consistency with the [1.1 First Edition specification](http://go.microsoft.com/fwlink/p/?linkid=203737).

-   **SVGInvalidValueError**

is raised when an invalid value is passed to an operation or assigned to an attribute.

-   **SVGMatrixNotInvertableError** is raised when an application tries to invert a matrix that is not invertible.

**Note:** The unusual spelling of this constant is maintained for compatibility with existing content.

### Standards information

-   [Scalable Vector Graphics (SVG) 1.1](http://go.microsoft.com/fwlink/p/?linkid=190918), Appendix B.4

### Members

The **SVGException** object has these methods:

-   [**toString**](/svg/methods/toString): Returns a string that represents the current object.

The **SVGException** object has these properties:

-   [**code**](/svg/properties/code): Gets the exception code that is raised.
-   [**message**](/svg/properties/message): Gets a description of the exception that is raised.
-   [**name**](/svg/properties/name): Gets the exception name that is raised.

## See also

### Related pages (MSDN)

-   DOM Exception Error Codes
