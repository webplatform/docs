---
title: length
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Not Ready'
standardization_status: 'W3C Recommendation'
summary: 'The number of nodes in the list.'
code_samples:
  - 'http://result.webplatformstaging.org/gist/66472399f3509d96204a/37c44f44eee101bcc19487fd1cf470e8a5c998d8'
uri: apis/NodeList/length

---
# length

## Summary

The number of nodes in the list.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/NodeList](/dom/NodeList)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = list.length;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">unsigned long</span></span>

## Examples

``` {.html}
<!-- Three divs -->
<ul>
    <li class="fruit">Apple</li>
    &li;class="fruit">Banana</li>
    <li class="fruit">Cherry</li>
</ul>
<div id="fruit"></div>

<script>
    // Query the DOM for the nodes with the class 'fruit'
    var fruitNodes = document.querySelectorAll('.fruit');

    // Get the number of nodes found by using 'length'
    var fruitNodeCount = fruitNodes.length;

    // Displaying the value in the DOM
    document.getElementById('fruit').innerHTML = 'Number of fruit nodes: ' + fruitNodeCount;

// Number of fruit nodes: 3
</script>
```

[View live example](http://result.webplatformstaging.org/gist/66472399f3509d96204a/37c44f44eee101bcc19487fd1cf470e8a5c998d8)

## Related specifications

Specification
:   Status
[DOM Level 1](http://www.w3.org/TR/REC-DOM-Level-1/level-one-core.html#ID-536297177)
:   Recommendation
[DOM](http://www.w3.org/TR/dom/#nodelist)
:   Working Draft

