{{Page_Title}}
{{Flags
|High-level issues=Stub, Needs Topics, Missing Relevant Sections
|Content=Incomplete
|Checked_Out=Yes
}}
{{API_Name}}
{{Summary_Section|This is an HTML hack to make pages more friendly to those without JS enabled or without JS support.}}
{{Concept_Page
|Content=This HTML hack makes it so users without JavaScript support or with JavaScript disabled can still view the normal content. Add this tag to the HTML head (best after the <meta charset="..." /> tag) and it will create an automatic redirect to the no-JS-friendly site:

<noscript><meta http-equiv="refresh" content="0;url=www.example.com/no-js-version" /></noscript>

This would alleviate the need for JavaScript to be required for many services to even be used, and it would allow for some degree of dynamic content to still be served to those without JS through CSS and server-side logic.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=Usage example of this hack (JS version).
|Code=<!-- www.example.com/index.html -->
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8" />
<noscript><meta http-equiv="refresh" content="0;url=www.example.com/no-js-version.html" /></noscript>
<script type="javascript" src="www.example.com/js/jquery.min.js"></script>
<script type="javascript" src="www.example.com/js/dynamic.js"></script>
<title>Example Page</title>
</head>
<body></body>
</html>
}}{{Single Example
|Language=JavaScript
|Description=Little helper dynamic script
|Code=// www.example.com/js/dynamic.js
$(function () {
  var div = document.createElement('div');
  div.innerHTML = 'someContent';
  $(body).append(div);
})();
}}{{Single Example
|Language=HTML
|Description=Non-JS version
|Code=<!-- www.example.com/no-js-version.html -->
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8" />
<title>Example Page</title>
</head>
<body>
<div>some content</div>
</body>
</html>
|LiveURL=www.example.com/no-js-version.html
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}