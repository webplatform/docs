{{Page_Title}}
{{Flags}}
{{API_Name}}
{{Summary_Section}}
{{Concept_Page
|Content='''Minification''' is the process of transforming a file in a way such that while the functionality of the input file are kept unchanged, the resulting file is much smaller. In the context of JavaScript and web applications, minification is especially useful because it reduces the amount of data that is necessary to transport across the Internet, and as such, reduces page load times.

Minification is usually accomplished by parsing code, then outputting it again in a compressed format. This code is generally unreadable with the naked eye. This process usually removes all white spaces, comments, and new line characters. Many other optimizations can also be performed, such as removing block delimiters, inlining functions, using implicit conditionals, and rewriting local variables.

In large projects, minification is often used automatically as part of a build process. Several JavaScript files can be combined together to reduce the overhead of multiple HTTP requests.

One of the advantages of code minification is that it can also be used to validate code. The minifier will alert you if your code is invalid, because invalid code obviously cannot be properly parsed and minified.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|External_links=* [http://en.wikipedia.org/wiki/Minification_(programming) Wikipedia: Minification (programming)]
* Minifiers
** [http://lisperator.net/uglifyjs/ UglifyJS]
** [https://developers.google.com/closure/compiler/ Google Closure Compiler]
** [http://constellation.github.com/esmangle/ Esmangle]
** [http://yuilibrary.com/projects/yuicompressor/ YUI Compressor]
** [http://www.crockford.com/javascript/jsmin.html JSMin]
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}