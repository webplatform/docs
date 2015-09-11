---
title: propertyName
attributions:
  - 'Microsoft Developer Network: [[propertyName Property](http://msdn.microsoft.com/en-us/library/ie/hh772142(v=vs.85).aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/propertyNameEX.htm'
notes:
  - "Duplicate propertyName properties listed on the\nTransitionEvent Page.\nhttp://docs.webplatform.org/wiki/dom/TransitionEvent\n>>http://docs.webplatform.org/wiki/dom/TransitionEvent/propertyName\n\n>>http://docs.webplatform.org/wiki/dom/TransitionEvent/propertyName"
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/TransitionEvent
    href: /dom/TransitionEvent
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/TransitionEvent
standardization_status: Non-Standard
summary: 'Specifies or retrives a string containg the name of the changed property.'
tags:
  - API
  - Object
  - Properties
  - DOM
  - JavaScript
uri: dom/TransitionEvent/propertyName

---
## <span>Summary</span>

Specifies or retrives a string containg the name of the changed property.

Property of [dom/TransitionEvent](/dom/TransitionEvent)[dom/TransitionEvent](/dom/TransitionEvent)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = object.propertyName;
```

## <span>Return Value</span>

Returns an object of type StringString

The name of the CSS property associated with the transition.

## <span>Examples</span>

This example uses the [**onpropertychange**](/dom/Element/propertychange) event to change the value of the **propertyName** property. This example needs to be run on IE prior to version 9 in order to work properly.

``` html
<!DOCTYPE html>
<html lang="en">
<head>
<script>
    function inform() {
        //Get propertyName property
        alert(event.propertyName + " property has changed value");
    };

    function changeProperty() {
        btnProp.value = "This is the new VALUE";
    };

    function changeCSSProperty() {
        btnStyleProp.style.backgroundColor = "aqua";
    };
</script>
</head>
<body>
    <p>The event object property propertyName is used here to return which property has been altered.</p>
    <input
      id="btnProp"
      type="button"
      value="Click to change the VALUE property of this button"
      onclick="changeProperty()"
      onpropertychange="inform()"
    />
    <input
      id="btnStyleProp"
      type="button"
      value="Click to change the CSS backgroundColor property of this button"
      onclick="changeCSSProperty()"
      onpropertychange="inform()"
    />
</body>
</html>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/propertyNameEX.htm)

## <span>Notes</span>

### <span>Remarks</span>

You can alter the value of **propertyName** by using it with the [**onpropertychange**](/dom/Element/propertychange) event that is available only on IE\<9.

### <span>Syntax</span>

## <span>See also</span>

### <span>Related articles</span>

#### <span>Javascript</span>

-   **propertyName**

-   [Number](/javascript/Number)

-   [unicode](/javascript/RegExp/unicode)

-   [future reserved words](/javascript/future_reserved_words)
