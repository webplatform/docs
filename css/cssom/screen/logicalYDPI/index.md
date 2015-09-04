---
title: logicalYDPI
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
notes:
  - 'Needs spec reference, standardization status'
summary: 'Retrieves the screen''s vertical Dots Per Inch (DPI) value.'
uri: css/cssom/screen/logicalYDPI

---
# logicalYDPI

## Summary

Retrieves the screen's vertical Dots Per Inch (DPI) value.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[css/cssom/screen](/css/cssom/screen)</span></span>

## Syntax

``` {.js}
var result = element.logicalYDPI;
element.logicalYDPI = value;
```

## Examples

The following examples use the **logicalYDPI** property to retrieve the normal vertical DPI of the screen. The function in this example returns `1` if Internet Explorer is not adjusting the scale of the screen.

``` {.js}
<script>
  function fnScaleFactorY() {
    var nScaleFactor = screen.deviceYDPI / screen.logicalYDPI;
    return nScaleFactor;
  }
</script>
```

This example uses the [**-ms-zoom**](/css/selectors/zoom) property of the **BODY** element to adjust the scale of the document "manually" if Internet Explorer is not adjusting the scale of the screen and the user's vertical DPI is higher than normal. This is a simple but imprecise way to make a document look the same on higher resolution screens. You can achieve finer control over the layout of your documents by modifying the properties of individual elements or groups of elements.

``` {.js}
<script>
  // change layout on HighDPI screens when IE not scaling
  function fnScaleManually()
  {
    // normal DPI
    var constNorm = 96;

    // scaling is off and DPI higher than normal
    if ((screen.deviceYDPI == screen.logicalYDPI)
      && (screen.deviceYDPI > constNorm))
    {
      document.body.style.zoom =
        constNorm / screen.logicalYDPI;
    }
  }
</script>
```

## Notes

### Remarks

On most systems, there is no difference between horizontal and vertical DPI. The normal DPI on most Windows systems is 96. When Windows Internet Explorer is adjusting the scale of the screen, the value of this property does not equal the value of the **deviceYDPI** property. **logicalYDPI** was introduced in Microsoft Internet Explorer 6. For information about how Internet Explorer 6 and later can adjust the scale of the display on screens with higher-than-normal DPI, see Adjusting Scale for Higher DPI Screens.

### Standards information

There are no standards that apply here.

## See also

### Related pages (MSDN)

-   `screen`
-   `Reference`
-   `deviceXDPI`
-   `deviceYDPI`
-   `logicalXDPI`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

