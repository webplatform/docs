{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The its-term attribute is used to mark terms so they can be recognized during translation process. This helps to increase consistency of translation across different parts of the documentation.}}
{{Markup_Attribute
|Applies_to=http://docs.webplatform.org/wiki/dom/HTMLElement
|Content=The its-term attribute can contain "yes" or "no" values. Defintion of the term can be optionally linked by using its-term-info-ref attribute.

}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Code=<syntaxhighlight>
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>Terminology test: default</title>
  </head>
  <body>
    <p>We need a new <span its-term="yes">motherboard</span></p>
  </body>
</html>
</syntaxhighlight>
|LiveURL=http://code.webplatform.org/gist/8404173
}}
}}
{{Notes_Section
|Usage=Use its-term for all terms on your page especially if you expect your content being translated to other languages in the future.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Internationalization Tag Set (ITS) Version 2.0
|URL=http://www.w3.org/TR/its20/
|Status=W3C Recommendation
}}
}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|Internationalization}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}