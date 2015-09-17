---
title: 'instanceof'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/zh0zb36z(v=vs.94).aspx)'
compatibility:
  feature: instanceof
  topic: javascript
readiness: 'Ready to Use'
summary: 'Returns a Boolean value that indicates whether or not an object is an instance of a particular class.'
tags:
  - JS_Basic
uri: javascript/operators/instanceof

---
## Summary

Returns a Boolean value that indicates whether or not an object is an instance of a particular class.

## Syntax

    result = object instanceof class

**result**
:   Required. Any variable.

**object**
:   Required. Any object expression.

**class**
:   Required. Any defined object class.

## Examples

The following example shows how to use the **instanceof** operator.

``` js
function objTest(obj){
     var i, t, s = "";
     t = new Array();
     t["Date"] = Date;
     t["Object"] = Object;
     t["Array"] = Array;
         for (i in t){
             if (obj instanceof t[i]) {
                 s += "obj is an instance of " + i + "<br/>";
             }
             else {
                 s += "obj is not an instance of " + i + "<br/>";
         }
     }
     return(s);
 }

 var obj = new Date();
 document.write(objTest(obj));

 // Output:
 // obj is an instance of Date
 // obj is an instance of Object
 // obj is not an instance of Array
```

## Remarks

The **instanceof** operator returns true if object is an instance of class. It returns false if object is not an instance of class, or if object is null.

