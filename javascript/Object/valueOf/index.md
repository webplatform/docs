---
title: valueOf
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/ftx8swz5(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Returns the primitive value of the specified object.'
tags:
  - JS
  - Basic
uri: javascript/Object/valueOf

---
## <span>Summary</span>

Returns the primitive value of the specified object.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    object.valueOf( )

## <span>Examples</span>

The following example illustrates the use of the valueOf method with a date object.

``` js
var myDate = new Date();
 myDate.setFullYear(2100, 5, 5);
 if (myDate.getTime() == myDate.valueOf())
     document.write("values are the same");
 else
     document.write("values are different");

 // Output: values are the same
```

## <span>Remarks</span>

The required object reference is any intrinsic JavaScript object.

The **valueOf** method is defined differently for each intrinsic JavaScript object.

|Object|Return Value|
|:-----|:-----------|
|Array|Returns the array instance.|
|Boolean|The Boolean value.|
|Date|The stored time value in milliseconds since midnight, January 1, 1970 UTC.|
|Function|The function itself.|
|Number|The numeric value.|
|Object|The object itself. This is the default.|
|String|The string value.|

The **Math** and Error objects do not have a **valueOf** method.

## <span>See also</span>

### <span>Other articles</span>

-   [toString Method (Object)](/javascript/Object/toString)

