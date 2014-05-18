{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The '''translate''' attribute indicates whether the element’s content and attribute values should be translated or not.}}
{{Markup_Attribute
|Applies_to=[[dom/HTMLElement|HTMLElement]]
|Content=Two values allowed: "yes" and "no". The information will be inherited. When no translate flag is set, "yes" is default.

Some automated translation services apply "no" to elements like the code element.

Elements with translate attributes of different values may be nested to indicate a chunk of text that should be translated within a container that should not be translated, or vice versa.

Overwriting "no" with "yes" is not widely supported by translation services yet.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Code=<syntaxhighlight><p>The national motto of France is
<i lang="fr" translate="no">Liberté, Egalité, Fraternité</i>
(freedom, equality, brotherhood).</p></syntaxhighlight>
}}{{Single Example
|Language=HTML
|Code=<syntaxhighlight><code translate="no">
&lt;section id="translate-attribute"&gt;
&lt;h2&gt;<span translate="yes">The <span translate="no">translate</span> attribute&lt;h2&gt;
&lt;p&gt;<span translate="yes">The <span translate="no">translate</span> attribute indicates whether the element’s content and attribute values should be translated or not.</span>&lt;/p&gt;
&lt;/section&gt;
</code></syntaxhighlight>
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|External_links=[http://www.w3.org/International/questions/qa-translate-flag Using HTML's translate attribute]
}}
{{Topics|HTML, Internationalization}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}