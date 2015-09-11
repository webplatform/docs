---
title: abort
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/xhr/XMLHttpRequest
    href: /apis/xhr/XMLHttpRequest
standardization_status: 'W3C Working Draft'
summary: 'Stops an asynchronous XMLHttpRequest in progress.'
tags:
  0: API
  1: Object
  2: Methods
  4: XHR
uri: apis/xhr/XMLHttpRequest/abort

---
## <span>Summary</span>

Stops an asynchronous XMLHttpRequest in progress.

Method of [apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)[apis/xhr/XMLHttpRequest](/apis/xhr/XMLHttpRequest)

## <span>Syntax</span>

``` js
 .abort();
```

## <span>Return Value</span>

No return value

## <span>Examples</span>

``` js
function request() {
    var xhr = new XMLHttpRequest();
    xhr.open("GET", "http://localhost/test.xml", true);
    xhr.send();
    return xhr;
}

document.getElementById('submit').addEventListener('click', function () {
    var xhr = request(),
        submit = this,
        cancel = document.getElementById('cancel');

    function detach() {
        submit.removeEventListener('click', canceling, false);
        cancel.removeEventListener('click', canceling, false);
    }

    function canceling() {
        detach();
        xhr.abort();
    }

    // detach any remaining handlers after XHR finishes
    xhr.addEventListener('load', detach, false);

    // cancel if "Submit" is clicked again before XHR finishes
    submit.addEventListener('click', canceling, false);

    // cancel if "Cancel" is clicked
    cancel.addEventListener('click', canceling, false);
}, false);
```

## <span>Notes</span>

Calling **abort** resets the object; the **readyState** is changed to 0 (uninitialized). Calling it on an already aborted request throws an exception.

## <span>Related specifications</span>

[W3C XMLHttpRequest Specification](http://www.w3.org/TR/XMLHttpRequest/)
:   W3C Working Draft
