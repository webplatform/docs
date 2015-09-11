---
title: readystatechange
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Fires whenever the readyState of the request changes. Mostly used to determine whether the body of the response is available for handling.'
tags:
  - Events
  - API
  - XHR
uri: apis/xhr/XMLHttpRequest/readystatechange

---
## <span>Summary</span>

Fires whenever the readyState of the request changes. Mostly used to determine whether the body of the response is available for handling.

## <span>Overview Table</span>

<table class="wikitable">
<tr>
<th>
Synchronous

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Bubbles

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Target

</th>
<td>
apis/xhr/XMLHttpRequest

</td>
</tr>
<tr>
<th>
Cancelable

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Default action

</th>
<td>
</td>
</tr>
</table>
## <span>Examples</span>

The following script demonstrates how to set an asynchronous event handler that alerts the user when the **readyState** property of the request reaches complete (`4`). Note that you must set the event handler after calling **open**, which resets all properties of the **XMLHttpRequest** object to their initial value.

``` js
function reportStatus() {
    if (xhr.readyState == 4 /* complete */) {
        if (xhr.status == 200 || xhr.status == 304) {
            console.log("Transfer complete.");
        }
        else {
            // error occurred
        }
    }
}
var xhr = new XMLHttpRequest();
xhr.open("GET", "http://localhost/test.xml", true);
xhr.onreadystatechange = reportStatus;
xhr.send();
```

## <span>Related specifications</span>

[W3C XMLHttpRequest Specification](http://www.w3.org/TR/XMLHttpRequest/)
:   W3C Working Draft
