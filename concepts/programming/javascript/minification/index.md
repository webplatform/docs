---
title: 'Code minification'
readiness: 'In Progress'
summary: 'Minification is the process of transforming a file in a way such that while the functionality of the input file are kept unchanged, the resulting file is much smaller. In the context of JavaScript and web applications, minification is especially useful because it can help reduce page load times. In larger projects, minification is generally integrated into a build process.'
tags:
  - Concept_Pages
  - Needs_Examples
uri: concepts/programming/javascript/minification

---
## Summary

Minification is the process of transforming a file in a way such that while the functionality of the input file are kept unchanged, the resulting file is much smaller. In the context of JavaScript and web applications, minification is especially useful because it can help reduce page load times. In larger projects, minification is generally integrated into a build process.

## Process

Minification is usually accomplished by parsing code, then outputting it again in a compressed format. This code is generally unreadable with the naked eye. This process usually removes all white spaces, comments, and new line characters. Many other optimizations can also be performed, such as removing block delimiters, inlining functions, using implicit conditionals, and rewriting local variables.

Several code constructs, however, prevent effective minification. The notorious \`eval()\` function can access any variables in its scope or global variables, and its contents cannot be known until runtime. Therefore, it's impossible to perform renaming optimizations on certain sections of code that use \`eval()\`.

Large projects usually integrate minification as part of their build process. They may also combine multiple JavaScript files to be minified together, reducing the overhead of HTTP requests.

## Advantages

Because minification reduces the size of code, minified code requires less data to be transferred. As a result, it loads faster, helping to decrease page load times. Another advantage of code minification is that it can also be used to validate code. The minifier will alert you if your code is invalid, because invalid code obviously cannot be properly parsed and minified.

## History

Douglas Crockford's JSMin, introduced in 2003, was the first JavaScript minifier. It simply removed comments and unnecessary whitespace from code. Soon after, Yahoo's YUI Compressor was introduced, which actually parsed code, and performed several other optimizations.

## See also

### External resources

-   [Wikipedia article](http://en.wikipedia.org/wiki/Minification_(programming))
-   Minifiers
    -   [UglifyJS](http://lisperator.net/uglifyjs/)
    -   [Google Closure Compiler](https://developers.google.com/closure/compiler/)
    -   [Esmangle](http://constellation.github.com/esmangle/)
    -   [YUI Compressor](http://yuilibrary.com/projects/yuicompressor/)
    -   [JSMin](http://www.crockford.com/javascript/jsmin.html)
