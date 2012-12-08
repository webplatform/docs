{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Deprecated}}
{{API_Name}}
{{Summary_Section|Use the [[html/attributes/type (script element)|type]] attribute instead. Specifies the language of the script to be evaluated. May be omitted when using ECMAScript (also known as JavaScript).}}
{{Markup_Attribute
|Applies_to=dom/HTMLScriptElement
|Property_applies_to=dom/HTMLScriptElement
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=Use this attribute only when you want the browser to evaluate the script in a language or a version of the language other than the default. If the browser does not support the specified language or version of the language, the script will not be evaluated.
|Notes=*See the [[html/attributes/lang|lang]] attribute if you want to declare the natural language of your content, eg. French, etc.
*When a [[html/attributes/type|type]] attribute is also specified, it takes precedence over this attribute and this attribute will be ignored.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Note=The default language is JScript (an implementation of ECMAScript, also known as JavaScript).
}}{{Compatibility Notes Row
|Browser=Internet Explorer
|Version=4 - 9
|Note=Include a JScript engine, as well as a VBScript engine.
}}{{Compatibility Notes Row
|Browser=Internet Explorer
|Version=5
|Note=Accepts a value of "XML".
}}{{Compatibility Notes Row
|Browser=Mozilla Firefox
|Note=Accepts "JavaScript", or a value that features a specific version, like "JavaScript1.5".
}}
}}
{{See_Also_Section}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}