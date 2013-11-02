{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Needs Review
|Content=Incomplete, Cleanup, Broken Links, Compatibility Incomplete
|Checked_Out=No
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|The '''menu''' element represents information as a list of items or commands.}}
{{Markup_Element
|DOM_interface=dom/HTMLMenuElement
|Content=The menu element is used to define a list as a menu of commands. The menu element has two specific attributes as well as can accept global and event attributes in HTML.

The '''menu''' element is currently unsupported by major browsers.

===Attributes===

The '''menu''' element will specifically accept the '''label''' attribute whose value is ''text'' and the '''type''' attribute whose value can be ''context'', ''toolbar'', or ''list''. ''list'' is the default value.

The '''menu''' element also accepts [[html/global_attributes | global attributes]] and [[html/event_attributes | event attributes]].
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This is an example of the '''menu''' element using the ''type'' and  ''label'' attributes as well as the '''button''' element.
|Code=<menu type="toolbar">
<li>
<menu label="File">
<button type="button" onclick="file_new()">New...</button>
<button type="button" onclick="file_open()">Open...</button>
<button type="button" onclick="file_save()">Save</button>
</menu>
</li>
<li>
<menu label="Edit">
<button type="button" onclick="edit_cut()">Cut</button>
<button type="button" onclick="edit_copy()">Copy</button>
<button type="button" onclick="edit_paste()">Paste</button>
</menu>
</li>
</menu>
|LiveURL=http://code.webplatform.org/gist/7284273
}}
}}
{{Notes_Section
|Usage=The '''menu''' element is currently unsupported by major browsers.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/
|Status=Deprecated
}}{{Related Specification
|Name=DOM HTML
|URL=http://www.w3.org/TR/DOM-Level-2-HTML/html
|Status=Redifined
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=HTML
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}