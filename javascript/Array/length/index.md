---
title: length
tags:
  0: JS
  1: Basic
  3: Property
readiness: 'Ready to Use'
summary: 'Basically specifies the number of elements (AKA length) in an Array object. This means the length property represents a number one greater than the largest index defined in an Array object.'
code_samples:
  - 'http://gist.github.com/9086506'
  - 'http://gist.github.com/9086602'
uri: javascript/Array/length

---
# length

## Summary

Basically specifies the number of elements (AKA length) in an Array object. This means the length property represents a number one greater than the largest index defined in an Array object.

## Syntax

    arrayObj.length;
    arrayObj.length = numVar;

**arrayObj**
:   Required. Any Array object.

**numVar**
:   Required. Any number less than 2 to the 32nd power (2\^32).

## Return Value

Any number less than 2 to the 32nd power (2\^32). The type of its value must be the unsigned 32 bit integer in the range 0 through 4294967295, inclusive.

## Examples

The array classes represents the content list of some training course. They are all displayed in the console by iterating over the array classes.

``` {.js}


var classes = ["HTML", "CSS", "JavaScript"];
document.write("This course includes:<br>");
for (var i = 0, j = classes.length; i < j; i++) {
    document.write(classes[i] + "<br>");
}
// Output:
// This course includes:
// HTML
// CSS
// JavaScript
```

</pre>
[View live example](http://code.webplatform.org/gist/9086506)

This shows how to limit the number of items added into a shopping cart. The length property shortens the array cart to a length of 3 if the current length is larger than 3. The attributes of the **length** property are { Writable: true, Enumerable: false, Configurable: false }. So you can set the **length** property to extend or truncate an Array object at any time.

``` {.js}
var cart = ["bread", "cheese", "coffee"];

cart.push("salad"); // length = 4
if (cart.length > 3) {
    alert("Don't add more than 3 items!");
    cart.length = 3;
    document.write(cart);
}

// Output: bread,cheese,coffee
```

[View live example](http://code.webplatform.org/gist/9086602)

## Remarks

In JavaScript arrays are sparse, and the elements in an array do not have to be contiguous. The **length** property is not necessarily the number of elements in the array. For example, in the following array definition, `my_array.length` contains 7, not 2:

    var my_array = new Array( );
    my_array[0] = "Test";
    my_array[6] = "Another Test";
    console.log(my_array.length);

    // Output
    // 7

Even if you set length to a number greater than its previous value, the number of actual elements does not increase.

    console.log(my_array.length); // 7
    my_array.length = 10;
    console.log(Object.keys(my_array));

    // Output
    // ["0", "6"]

On the other hand, when decreasing length, the array is truncated.

    console.log(my_array.length); // 10
    my_array.length = 1;
    console.log(Object.keys(my_array));

    // Output
    // ["0"]

## See also

### External resources

-   [JavaScript, by Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/length)
-   [Relationship between length and numerical properties, by Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array#Relationship_between_length_and_numerical_properties)

### Specification

[15.4.5.2 length](http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.5.2)

ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/d8ez24f2(v=vs.94).aspx)

