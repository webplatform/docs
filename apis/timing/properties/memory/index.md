---
title: performance.memory
attributions:
  - 'Microsoft Developer Network.'
notes:
  - 'Not part of user_timing, resource_timing, or navigation_timing interfaces. Experimental; deletion candidate'
readiness: 'Not Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/timing
    href: '/w/index.php?title=apis/timing&action=edit&redlink=1'
  return:
    predicate: 'Returns an object of type '
    value: Object
    href: '/w/index.php?title=apis/timing&action=edit&redlink=1'
standardization_status: Non-Standard
summary: 'Do not use. Proprietary. Chrome only. Gets quantized scripting memory usage numbers.'
tags:
  - API
  - Object
  - Properties
  - DOM
  - Performance
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - apis/timing
uri: apis/timing/properties/memory

---
## <span>Summary</span>

Do not use. Proprietary. Chrome only. Gets quantized scripting memory usage numbers.

Property of [apis/timing](/w/index.php?title=apis/timing&action=edit&redlink=1)[apis/timing](/w/index.php?title=apis/timing&action=edit&redlink=1)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var memoryInfo = window.performance.memory;
```

## <span>Return Value</span>

Returns an object of type ObjectObject

An object created with *MemoryInfo* constructor, containing *jsHeapSizeLimit*, *totalJSHeapSize* and *usedJSHeapSize* properties with numerical values.

## <span>Examples</span>

``` js
console.log(performance.memory)

// Would show, for example
//{
// jsHeapSizeLimit: 767557632,
// totalJSHeapSize: 58054528,
// usedJSHeapSize: 42930044
//}
```

## <span>Notes</span>

*usedJsHeapSize* is the total amount of memory being used by JS objects including V8 internal objects, *totalJsHeapSize* is current size of the JS heap including free space not occupied by any JS objects. This means that *usedJsHeapSize* can not be greater than *totalJsHeapSize*. Note that it is not necessarily that there has ever been *totalJsHeapSize* of alive JS objects.

The values are quantized as to not expose private information to attackers. If Chrome is run with the flag \`--enable-precise-memory-info\` the values are not quantized.

 See the [WebKit Patch](https://bugs.webkit.org/attachment.cgi?id=154876&action=prettypatch) for how the quantized values are exposed. The tests in particular help explain how it works.

-   [WebKit bug](https://bugs.webkit.org/show_bug.cgi?id=86636)
