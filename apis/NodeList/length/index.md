---
title: length
code_samples:
  - 'http://result.webplatformstaging.org/gist/66472399f3509d96204a/37c44f44eee101bcc19487fd1cf470e8a5c998d8'
readiness: 'Not Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/NodeList
    href: /dom/NodeList
  return:
    predicate: 'Returns an object of type '
    value: 'unsigned long'
    href: /dom/NodeList
standardization_status: 'W3C Recommendation'
summary: 'The number of nodes in the list.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: apis/NodeList/length

---
## Summary

The number of nodes in the list.

Property of [dom/NodeList](/dom/NodeList)[dom/NodeList](/dom/NodeList)

## Syntax

**Note**: This property is read-only.

``` js
var result = list.length;
```

## Return Value

Returns an object of type unsigned longunsigned long

## Examples

``` html
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

[DOM Level 1](http://www.w3.org/TR/REC-DOM-Level-1/level-one-core.html#ID-536297177)
:   Recommendation

[DOM](http://www.w3.org/TR/dom/#nodelist)
:   Working Draft
