---
title: for in
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/55wb2d34(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Executes one or more statements for each property of an object, or each element of an array.'
tags:
  - JS
  - Basic
uri: 'javascript/statements/for in'

---
## <span>Summary</span>

Executes one or more statements for each property of an object, or each element of an array.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    for ( variable in [ object | array ]) {
        statements
    }

**variable**
:   Required. A variable that can be any property name of object or any element index of an array.

**object , array**
:   Optional. An object or array over which to iterate.

**statements**
:   Optional. One or more statements to be executed for each property of object or each element of array. Can be a compound statement.

## <span>Examples</span>

The following example illustrates the use of the for...in statement with an object used as an associative array.

``` js
// Initialize object.
 a = {"a" : "Athens" , "b" : "Belgrade", "c" : "Cairo"}

 // Iterate over the properties.
 var s = ""
 for (var key in a) {
     s += key + ": " + a[key];
     s += "<br />";
 }
 document.write (s);

 // Output:
 // a: Athens
 // b: Belgrade
 // c: Cairo
```

This example illustrates the use of the for ... in statement to iterate though an **Array** object that has expando properties.

``` js
// Initialize the array.
 var arr = new Array("zero","one","two");

 // Add a few expando properties to the array.
 arr["orange"] = "fruit";
 arr["carrot"] = "vegetable";

 // Iterate over the properties and elements.
 var s = "";
 for (var key in arr) {
     s += key + ": " + arr[key];
     s += "<br />";
 }

 document.write (s);

 // Output:
 //   0: zero
 //   1: one
 //   2: two
 //   orange: fruit
 //   carrot: vegetable
```

## <span>Remarks</span>

At the beginning of each iteration of a loop, the value of variable is the next property name of object or the next element index of array. You can then use variable in any of the statements inside the loop to reference the property of object or the element of array.

The properties of an object are not assigned in a determinate manner. You cannot specify a particular property by its index, only by the name of the property.

Iterating through an array is performed in element order, that is, 0, 1, 2.

## <span>Notes</span>

Use the **Enumerator** object to iterate over the members of a collection.

## <span>See also</span>

### <span>Other articles</span>

-   [for Statement](/javascript/statements/for)
-   [while Statement](/javascript/statements/while)

