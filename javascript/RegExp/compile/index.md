---
title: compile
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/x9cswe0z(v=vs.94).aspx)'
notes:
  - 'Moved under javascript/RegExp'
readiness: 'Ready to Use'
summary: 'Compiles a regular expression into an internal format for faster execution.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/RegExp/compile

---
## Summary

Compiles a regular expression into an internal format for faster execution.

## Syntax

<span class="language">JavaScript</span>

    rgExp.compile( pattern , [ flags ] )

**rgExp**
:   Required. An instance of a **Regular Expression** object. Can be a variable name or a literal.

**pattern**
:   Required. A string expression containing a regular expression pattern to be compiled

**flags**
:   Optional. Available flags, which may be combined, are: `g` (global search for all occurrences of the pattern), `i` (ignore case), `m` (multiline search), `u` (Unicode), `y` (sticky matching),

## Examples

The following example illustrates the use of the **compile** method:

``` js
function CompileDemo(){
    var rs;
    var s = "AaBbCcDdEeFfGgHhIiJjKkLlMmNnOoPp"
    // Create regular expression for uppercase only.
    var r = new RegExp("[A-Z]", "g");
    var a1 = s.match(r)              // Find matches.
    // Compile the regular expression for lowercase only.r.compile( "[a-z]" , "g" ) ;
 // Find matches.
    var a2 = s.match(r)
    return(a1 + "\n" + a2);
 }
```

## Remarks

The **compile** method converts pattern into an internal format for faster execution. This allows for more efficient use of regular expressions in loops, for example. A compiled regular expression speeds things up when reusing the same expression repeatedly. No advantage is gained, however, if the regular expression changes.

