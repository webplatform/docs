---
title: '1...9 Properties'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/24th3sah(v=vs.94).aspx)'
compatibility:
  feature: '1 9 Properties'
  topic: javascript
readiness: 'Ready to Use'
summary: 'Return the nine most-recently memorized portions found during pattern matching. Read-only.'
tags:
  - JS
  - Basic
uri: 'javascript/RegExp/1 9 Properties'

---
## Summary

Return the nine most-recently memorized portions found during pattern matching. Read-only.

## Syntax

    RegExp.$ n

'***RegExp'***
:   Always the global **RegExp** object.

**n**
:   Any integer from 1 through 9.

## Examples

The following example performs a regular expression search. It displays matches and submatches from the global **RegExp** object. The submatches are successful parenthesized matches that are contained in the **...** properties. The example also displays matches and submatches from the array that is returned by the **exec** method.

``` js
var newLine = "<br />";

 var re = /(\w+)@(\w+)\.(\w+)/g
 var src = "Please send mail to george@contoso.com and someone@example.com. Thanks!"

 var result;
 var s = "";

 // Get the first match.
 result = re.exec(src);

 while (result != null) {
     // Show the entire match.
     s += newLine;

     // Show the match and submatches from the RegExp global object.
     s += "RegExp.lastMatch: " + RegExp.lastMatch + newLine;
     s += "RegExp.: " + RegExp. + newLine;
     s += "RegExp.: " + RegExp. + newLine;
     s += "RegExp.: " + RegExp. + newLine;

     // Show the match and submatches from the array that is returned
     // by the exec method.
     for (var index = 0; index < result.length; index++) {
         s +=  index + ": ";
         s += result[index];
         s += newLine;
     }

     // Get the next match.
     result = re.exec(src);
 }
 document.write(s);

 // Output:
 //  RegExp.lastMatch: george@contoso.com
 //  RegExp.: george
 //  RegExp.: contoso
 //  RegExp.: com
 //  0: george@contoso.com
 //  1: george
 //  2: contoso
 //  3: com

 //  RegExp.lastMatch: someone@example.com
 //  RegExp.: someone
 //  RegExp.: example
 //  RegExp.: com
 //  0: someone@example.com
 //  1: someone
 //  2: example
 //  3: com
```

## Remarks

The values of the **\$1...\$9** properties are modified whenever a successful parenthesized match is made. Any number of parenthesized substrings may be specified in a regular expression pattern, but only the nine most recent can be stored.

