{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Update/improve example;
|Checked_Out=No
}}
{{Standardization_Status|W3C Proposed Recommendation}}
{{API_Name}}
{{Summary_Section|Provides additional control over when an external script is being fetched and executed while a document loads.}}
{{Markup_Attribute
|Applies_to=
|Property_applies_to=dom/HTMLElement
|Content=Usually <code><script></code> elements bring a browser's HTML parser to a temporary halt until the contained or referenced script has been fetched and has also been fully executed. The <code>async</code> attribute decouples script fetching and execution from the main process of HTML parsing which enables the browser to continue rendering the underlaying page at full speed. 
A script marked with the <code>async</code> attribute will be fetched and executed at some later point in time upon which the browser is free to decide. In most cases this will be as soon as the browser finds an opportunity to request it. In addition to that such a script will also no longer respect the order in which the <code><script></code> elements were initially declared in the HTML source. This means that there shouldn't be other script that depend or build upon scripts marked as asynchronous.
It is also important to know that the <code>async</code> attribute only works for externally referenced scripts. When attached to an inline script block this attribute is simply ignored.
And finally asynchronous scripts are no longer part of the content relevant to firing the <code>DOMContentLoaded</code> event. But they are still part of the global <code>load</code> event.

==Programmatically created Scripts==

All of the above only applies to scripts declared via HTML markup. For scripts created via JavaScript the effects are sort of turned upside down. The first change is that dynamically created scripts always start off by being fully asynchronous, meaning they neither block the HTML parser nor do they respect their order of creation. The effect is the same as if one would set <code>script.async = true;</script>. What is possible here is to set <code>script.async = false;</script>. This won't bring the script all the way back to a point where it would block the HTML parser, but it does make the script respect the order of creation. This allows one to work with dependancies between dynamically created scripts. Beware: "order of creation" doesn't factor in any scripts declared via HTML. Declarative scripts and programmatic scripts both live in their own worlds.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=
|Notes=Setting a script to run asynchronously can improve performance by unblocking the rest of the document. When async = false, it can preserve execution order to ensure dependent scripts are run in order.
|Import_Notes====Syntax===
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML5
|URL=http://www.w3.org/TR/html5/scripting-1.html#attr-script-async
|Status=W3C Proposed Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Topic_clusters=Javascript, Performance
|Manual_links=
|External_links=
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/HTMLScriptElement|HTMLScriptElement]]</code>
}}
{{Topics|HTML, JavaScript, Performance}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=8
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=3.6
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=3
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=10
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=Beta
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=14
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=No
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=5
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}