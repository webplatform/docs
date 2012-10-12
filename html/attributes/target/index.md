{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Markup_Attribute
|Applies_to=http://docs.webplatform.org/wiki/html/elements/a
|Property_applies_to=dom/HTMLElement
|Content=<strong>Target</strong> is a link attribute that defines in what window a link will open. 
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=A target value of "_blank" will cause the page to open in a new window. 
|Code=<syntaxhighlight lang="html5"><a href="#" target="_blank">Link Text</a></syntaxhighlight>
}}{{Single Example
|Language=HTML
|Description=A target value of "_self" will cause the page to open in the same window or frame. 
|Code=<syntaxhighlight lang="html5"><a href="#" target="_self">Link Text</a></syntaxhighlight>
}}{{Single Example
|Language=HTML
|Description=A target value of "_parent" will cause the page to open in parent frame of the element. 
|Code=<syntaxhighlight lang="html5"><a href="#" target="_parent">Link Text</a></syntaxhighlight>
}}{{Single Example
|Language=HTML
|Description=A target value of "_top" will cause the page to open in the top-most frame. 
|Code=<syntaxhighlight lang="html5"><a href="#" target="_top">Link Text</a></syntaxhighlight>
}}
}}
{{Notes_Section
|Notes====Remarks===
The window '''name''' is an optional argument in the [[dom/methods/open|'''open''']] scripting method.
If there is no existing window or frame with the same '''name''' as specified in the '''target''', a new window is opened with a '''name''' equal to the value of the '''target'''.

|Import_Notes====Syntax===
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[html/elements/a|a]]</code>
*<code>area</code>
*<code>base</code>
*<code>form</code>
*<code>link</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}