---
title: Comment
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer JavaScript reference Article](http://msdn.microsoft.com/en-us/library/ie/yek4tbz0%28v=vs.94%29.aspx)'
notes:
  - 'Todo: Probably should be renamed to ''comment'' instead of ''Comment'''
readiness: 'Ready to Use'
summary: 'Causes comments to be ignored by the JavaScript parser.'
tags:
  - JS
  - Basic
uri: javascript/statements/Comment

---
## Summary

Causes comments to be ignored by the JavaScript parser.

## Syntax

    Single-line Comment:
    // comment

    Multiline Comment:
    /*
    comment
    */

    Comments with conditional compilation:
    //@CondStatement
    /*@
    condStatement
    @*/

## Examples

The following example illustrates the most common uses of comments.

``` js
/* This is a multiline comment that
     can span as many lines as necessary.  */
 function myfunction(arg1, arg2){
     var r;
     // This is a single line comment.
     r = arg1 + arg2
     return(r);
 }
```

The following example shows how to use conditional compilation. This example uses special comment delimiters that are used only if conditional compilation is activated by the @cc\_on statement. Scripting engines that do not support conditional compilation see only the message that says conditional compilation is not supported.

``` js
/*@cc_on @*/
 /*@if (@_jscript_version >= 4)
     alert("JavaScript version 4 or better");
     @else @*/
     alert("Conditional compilation not supported by this scripting engine.");
 /*@end @*/
```

## Remarks

The comment argument is the text of any comment you want to include in your script. The condStatement argument is to be used if conditional compilation is activated. If single-line comments are used, there can be no space between the "//" and "@" characters.

Use comments to keep parts of a script from being read by the JavaScript parser. You can use comments to include explanatory remarks in a program.

If single-line comments are used, the parser ignores any text between the comment marker and the end of the line. If multi-line comments are used, the parser ignores any text between the beginning and end markers.

Comments are used to support conditional compilation while retaining compatibility with browsers that do not support that feature. These browsers treat those forms of comments as single-line or multi-line comments respectively.

