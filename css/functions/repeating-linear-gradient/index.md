---
title: repeating-linear-gradient
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Examples needed.'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: css/functions/
    href: '/w/index.php?title=css/functions/&action=edit&redlink=1'
tags:
  - API
  - Object
  - Properties
  - DOM
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - css/functions/
uri: css/functions/repeating-linear-gradient

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [css/functions/](/w/index.php?title=css/functions/&action=edit&redlink=1)[css/functions/](/w/index.php?title=css/functions/&action=edit&redlink=1)

## <span>Syntax</span>

``` js
var result = element.repeating-linear-gradient;
element.repeating-linear-gradient = value;
```

**Needs Examples**: This section should include examples.

## <span>Notes</span>

### <span>Remarks</span>

Once the last color stop has been reached, the gradient starts again at the first color stop and repeats. It's a good idea to specify identical colors for the first and last color stops to prevent abrupt color changes between each repeating group. The syntax for the **repeating-linear-gradient** function is identical to that of the [**linear-gradient**](/css/linear-gradient) function. **Important**  The Cascading Style Sheets (CSS) Gradients properties do not require a vendor prefix (that is, "-ms-") to work correctly in Internet Explorer 10. The syntax for the **repeating-linear-gradient** function given in this topic is different from that supported in previous pre-releases of Internet Explorer 10, which required the "-ms-" prefix. To maximize backward compatibility, those older implementations are still recognized, as described in [**-ms-repeating-linear-gradient**](/css/properties/-ms-repeating-linear-gradient).

### <span>Syntax</span>

**repeating-linear-gradient** `([ [  <angle>  | to  <side-or-corner>  ] , ] ?  <color-stop>  [ ,   <color-stop>  ] +)`

### <span>Parameters</span>

*angle*
:   Optional. The angle the gradient line should assume, expressed as a number followed by an angle units designator(for instance, "deg")."0deg" points upward and positive angles increase in a clockwise direction. Therefore, "90deg" points toward the right, "180deg" points downward, and so on.If no angle is provided, the gradient line starts in the corner or side opposite the corner or side specified by *\<side-or-corner\>*.
*side-or-corner*
:   Optional value that specifies an corner point or side for the gradient. This value begins with "to", which is followed by one or two of the following keywords. Including one keyword specifies an ending side, and two keywords specify an ending corner.
    -   The following values can be used as the first value only:
        -   **left**  First value only. Indicates gradient ends on the left.
        -   **right**  First value only. Indicates gradient ends on the right.
    -   The following values can be used as the second value only:
        -   **top**  Second value only. Indicates gradient ends on the top.
        -   **bottom**  Second value only. Indicates gradient ends on the bottom.
    -   Not including any keywords or angle is equivalent to "to bottom".

*color-stop*
:   At least two color stops are required. Each color stop has one or two components—a color component and an optional position component. The first component defines the color component of a stop point for the gradient. Each stop point has its own designated color, and the area between each point is filled with a continuous color transition from one to the other. This value can be any supported color value.Each stop point can have an optional percentage or supported length value that indicates where along the gradient line to place the color stop. "0%" (or "0px", "0em", and so on) indicates the starting point (or side); "100%" indicates the ending point (or side).

## <span>See also</span>

### <span>Related articles</span>

#### <span>Gradients</span>

-   [linear-gradient](/css/functions/linear-gradient)

-   [css/functions/radial-gradient](/css/functions/radial-gradient)

-   **repeating-linear-gradient**

-   [repeating-radial-gradient](/css/functions/repeating-radial-gradient)

-   [-ms-radial-gradient](/css/properties/-ms-radial-gradient)

-   [-ms-repeating-linear-gradient](/css/properties/-ms-repeating-linear-gradient)

-   [-ms-repeating-radial-gradient](/css/properties/-ms-repeating-radial-gradient)
