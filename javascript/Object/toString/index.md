---
title: 'toString'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/k6xhc6yc(v=vs.94).aspx)'
compatibility:
  feature: toString
  topic: javascript
readiness: 'Ready to Use'
summary: 'Returns a string representation of an object.'
tags:
  - JS_Basic
uri: javascript/Object/toString

---
## Summary

Returns a string representation of an object.

## Syntax

    objectname.toString([ radix ])

**objectname**
:   Required. An object for which a string representation is sought.

**radix**
:   Optional. Specifies a radix for converting numeric values to strings. This value is only used for numbers.

## Examples

The following example illustrates the use of the **toString** method with a radix argument. The return value of function shown below is a Radix conversion table.

``` js
function CreateRadixTable (){
    var s = "";

    // Create table heading.
    s += "Hex  Dec  Bin \n";

    for (x = 0; x < 16; x++)
    {
       s += "   ";

       // Convert to hexidecimal.
       s += x.toString(16);
       s += "     ";
       if (x < 10) s += "  ";

       // Convert to decimal.
       s += x.toString(10);
       s += "     ";

       // Convert to binary.
       s += x.toString(2);
       s += "\n";
    }

    return(s);
 }
```

## Remarks

The **toString** method is a member of all built-in JavaScript objects. How it behaves depends on the object type:

|Object|Behavior|
|:-----|:-------|
|Array|Elements of an **Array** are converted to strings. The resulting strings are concatenated, separated by commas.|
|Boolean|If the Boolean value is **true** , returns " `true` ". Otherwise, returns " `false` ".|
|Date|Returns the textual representation of the date.|
|Error|Returns a string containing the associated error message.|
|Function|Returns a string of the following form, where functionname is the name of the function whose **toString** method was called:Copy Code function functionname( ) { [native code] }|
|Number|Returns the textual representation of the number.|
|String|Returns the value of the String object.|
|Default|Returns `"[object objectname]"` , where `objectname` is the name of the object type.|

## See also

### Other articles

-   [function Statement](/javascript/statements/function)

