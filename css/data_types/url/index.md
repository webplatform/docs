---
title: <url>
code_samples:
  - 'http://gist.github.com/10604525'
  - 'http://gist.github.com/10603403'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The &lt;url&gt; CSS data type, formerly called the &lt;uri&gt; data type, represents a reference to a file or file fragment.  It is specified with the url() function.'
tags:
  - Data
  - Type
  - CSS
uri: 'css/data types/url'

---
## <span>Summary</span>

The &lt;url&gt; CSS data type, formerly called the &lt;uri&gt; data type, represents a reference to a file or file fragment. It is specified with the url() function.

 The `url(string)` function identifies the parameter string as a resource identifier; possible resource identifier types include absolute file paths, relative file paths, fragment identifiers and data URI values. Relative file paths are resolved relative to the location of the file that contains the CSS rule.

The `<url>` data type is commonly used for images, but also for loading web fonts or defining filter or clipping path effects (in which case the identifier must link to a fragment within an SVG file).

The string may be quoted (with single or double quotes) but need not be. If an unquoted string contains any whitespace or special characters they will need to be escaped with a **\\** character; quoted strings require escapes for line breaks or for any nested quotes of the same type (see the third [example](#Examples)). See the [`<string>` data type page](/css/data_types/string) for more information on escape sequences for CSS strings.

Not all references in CSS to external files require the use of the `url()` syntax; file names in [`@import` rules](/css/atrules/@import), for example, may be given as simple quoted [`<string>`](/css/data_types/string) values.

## <span>Examples</span>

**Relative URLs and Fragments**

In a `<style>` block in an HTML or SVG page, relative files and fragments are resolved relative to that page or its base url.

``` html
<html>
<head>
   <style>
       body {
           background-image: url("fileInTheSameFolderAsThisPage.jpeg");
       }
       .blurry {
           filter: url("#blurFilter");
       }
   </style>
</head>
<body>
  <svg>
    <defs>
       <filter id="blurFilter">
          <feGaussianBlur stdDeviation="2"/>
       </filter>
    </defs>
  </svg>

  <h1 class="blurry">Blurry Headline</h1>

</body>
</html>
```

[View live example](http://code.webplatform.org/gist/10604525)

In an external stylesheet, relative files are resolved relative to the stylesheet's location.

``` css
body {
           background-image: url(fileInTheSameFolderAsTheStylesheet.jpeg);
    /* note that a simple file name does not have to be quoted */
}
```

**Escaped Characters and Data URIs**

The **\\** character allows you to escape the following character in a url string, allowing you to nest quotation marks (or you can simply use a different quotation mark type). To break a long string across multiple lines, use a **\\** escape character as the *final* character in each line.

**Note**: This example does not work in Internet Explorer, which does not support xml data URI values without full URI encoding.

``` css
ul.custom {
  font-size:x-large;
  list-style:image;
  list-style-image:url(
    "data:image/svg+xml;charset=UTF-8,\
    <svg xmlns=\"http://www.w3.org/2000/svg\" \
      width='100%' height='100%' \
      viewBox='-5 -5 10 10' preserveAspectRatio='xMidYMid meet'>\
        <circle r='4' fill='blue' stroke='green' stroke-width='2'/>\
    </svg>"
  );
}
```

[View live example](http://code.webplatform.org/gist/10603403)

## <span>Related specifications</span>

[CSS Values and Units Module Level 3](http://www.w3.org/TR/css3-values/#urls)
:   W3C Candidate Recommendation

[CSS 2.1](http://www.w3.org/TR/CSS21/syndata.html#uri)
:   W3C Recommendation
