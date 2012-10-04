{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Topics|HTML}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the '''TARGET''' attribute to specify a link that loads the page into the topmost frame of the current frameset.
|LiveURL=
|Code=
&lt;A HREF{{=}}"newpage.htm" TARGET{{=}}"_top"&gt;Go to  Page.&lt;/A&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The window '''name''' is an optional argument in the [[dom/methods/open|'''open''']] scripting method.
If there is no existing window or frame with the same '''name''' as specified in the '''target''', a new window is opened with a '''name''' equal to the value of the '''target'''.

Windows Internet Explorer 8 and later. When Protected Mode is enabled and a webpage contains an [[html/elements/a|'''anchor link''']] with a named '''target''', Windows Internet Explorer opens the target of the link in a new window when the target has a different integrity level than the webpage containing the link. For more information, see Understanding and Working in Protected Mode Internet Explorer.
In Internet Explorer 6, the  value of the '''target''' parameter of this property specifies that a linked document loads in the content area of the '''target'''.
In a Metro style app using JavaScript, if you set the  '''target''' attribute to the name of an '''iframe''',  the   '''iframe''' loads the linked document. If the specified '''target''' doesn't exist, the link opens in the default browser.
For more info about navigation in Metro style apps using JavaScript, see   Supporting navigation.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[html/elements/a|a]]</code>
*<code>area</code>
*<code>base</code>
*<code>form</code>
*<code>link</code>
|Topic_clusters=html
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}