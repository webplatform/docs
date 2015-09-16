---
title: 'random'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer JavaScript reference Article](http://msdn.microsoft.com/en-us/library/ie/yek4tbz0%28v=vs.94%29.aspx)'
compatibility:
  feature: random
  topic: javascript
readiness: 'Ready to Use'
summary: 'Returns a pseudorandom number between 0 and 1.'
tags:
  - JS
  - Basic
uri: javascript/Math/random

---
## Summary

Returns a pseudorandom number between 0 and 1.

## Syntax

    Math.random( )

## Examples

``` js
Math.random(); // 0.6236026335973293
Math.random(); // 0.10149288410320878
Math.random(); // 0.6313296002335846
```

## Remarks

The pseudo-random number generated is from 0 (inclusive) to 1 (exclusive), that is, the returned number can be zero, but it will always be less than one. The random number generator is seeded automatically when JavaScript is first loaded.

Due to the nature of the generation methods, these pseudo-random numbers are not uniformly distributed. They are normally distributed which means that, in general, a number is more likely to be closer to 0.5 than 0 or 1.

Note that this method is unsuitable for cryptography. The [WebCrypto API](https://dvcs.w3.org/hg/webcrypto-api/raw-file/tip/spec/Overview.html) addresses this.

## See also

### Other articles

-   [Math.pow Function](/javascript/Math/pow)

