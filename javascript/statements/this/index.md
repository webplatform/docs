---
title: 'this'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/w062xezx(v=vs.94).aspx)'
compatibility:
  feature: this
  topic: javascript
readiness: 'Ready to Use'
summary: 'Refers to the current object.'
tags:
  - JS
  - Basic
uri: javascript/statements/this

---
## Summary

Refers to the current object.

## Syntax

    this.property

## Examples

In the following example, **this** refers to the newly created Car object, and assigns values to three properties:

``` js
function Car(color, make, model){
    this.color = color;
    this.make = make;
    this.model = model;
 }
```

The **this** keyword generally refers to the **window** object if used outside of the scope of any other object. However, inside event handlers this refers to the DOM element that raised the event.

In the following code (for Internet Explorer 9 and later), the event handler prints the string version of a button that has an ID of "clicker".

``` js
document.getElementById("clicker").addEventListener("click", eventHandler, false);

         function eventHandler(ev) {
             document.write(this.toString());
         }

 // Output (when you click the button): [object HTMLButtonElement]
```

## Remarks

The required property argument is one of the current object's properties

The this keyword can be used in object constructors to refer to the current object.

## See also

### Other articles

-   [new Operator](/javascript/operators/new)

