{{Page_Title|&lt;url&gt;}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{Summary_Section|The <code>&lt;url></code> CSS data type, formerly called the <code>&lt;uri></code> data type, represents a reference to a file or file fragment.  It is specified with the [[css/functions/url()|<code>url()</code> function]].}}
{{Data_Type_Page
|Content=The <code>url(string)</code> function identifies the parameter string as a resource identifier; possible resource identifier types include absolute file paths, relative file paths, fragment identifiers and data URI values.   Relative file paths are resolved relative to the location of the file that contains the CSS rule.

The <code>&lt;url></code> data type is commonly used for images, but also for loading web fonts or defining filter or clipping path effects (in which case the identifier must link to a fragment within an SVG file).

The string may be quoted (with single or double quotes) but need not be.  If an unquoted string contains any whitespace or special characters they will need to be escaped with a '''\''' character; quoted strings require escapes for line breaks or for any nested quotes of the same type (see the third [[#Examples | example]]).  See the [[css/data_types/string | <code>&lt;string></code> data type page]] for more information on escape sequences for CSS strings. 

Not all references in CSS to external files require the use of the <code>url()</code> syntax; file names in [[css/atrules/@import |<code>@import</code> rules]], for example, may be given as simple quoted [[css/data_types/string| <code>&lt;string></code>]] values.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description='''Relative URLs and Fragments'''

In a <code>&lt;style></code> block in an HTML or SVG page, relative files and fragments are resolved relative to that page or its base url.
|Code=<html>
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
|LiveURL=http://code.webplatform.org/gist/10604525
}}{{Single Example
|Language=CSS
|Description=In an external stylesheet, relative files are resolved relative to the stylesheet's location.
|Code=body {
           background-image: url(fileInTheSameFolderAsTheStylesheet.jpeg);
    /* note that a simple file name does not have to be quoted */
}
}}{{Single Example
|Language=CSS
|Description='''Escaped Characters and Data URIs'''

The '''\''' character allows you to escape the following character in a url string, allowing you to nest quotation marks (or you can simply use a different quotation mark type).  To break a long string across multiple lines,  use a '''\''' escape character as the ''final'' character in each line.
{{Note|This example does not work in Internet Explorer, which does not support xml data URI values without full URI encoding.}}
|Code=ul.custom {
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
|LiveURL=http://code.webplatform.org/gist/10603403
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Values and Units Module Level 3
|URL=http://www.w3.org/TR/css3-values/#urls
|Status=W3C Candidate Recommendation
|Relevant_changes=Changed the type name to <code>&lt;url></code>
}}{{Related Specification
|Name=CSS 2.1
|URL=http://www.w3.org/TR/CSS21/syndata.html#uri
|Status=W3C Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}