{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add notes, compatibility.
|Checked_Out=No
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|The '''menu''' element represents information as a list of items or commands.}}
{{Markup_Element
|DOM_interface=dom/HTMLMenuElement
|Content=The menu element is used to define a list as a menu of commands. It can have event and global attributes in addition to two of its own.
 
The '''menu''' element has partial support in Firefox only for the context form.
 
===Attributes===
 
* ''label'' - Text for the label to display for the menu item.
* ''type'' - How the menu should be displayed to the user. Possible values are:
** ''context'' - Display a series of entries triggered by another element. Like a dropdown for example.
** ''list'' - Default. The name could change to ''toolbar'' in HTML 5.1. Displays menu items that are always within view.
 
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
|Usage=The '''menu''' and [[html/elements/ul|'''ul''']] both represent an unordered list of items. They differ in the way that the [[html/elements/ul|'''ul''']] element only contains items to display while the '''menu''' element contains interactive items, to act on.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/interactive-elements.html#the-menu-element
|Status=W3C Working Draft
}}
}}
{{See_Also_Section
|Manual_links=* [[html/elements/dir|<code>dir</code>]]
* [[html/elements/ul|<code>ul</code>]]
* [[html/elements/ol|<code>ol</code>]]
* [[html/elements/li|<code>li</code>]]
* [[html/elements/dl|<code>dl</code>]]
* [[html/elements/dt|<code>dt</code>]]
* [[html/elements/dd|<code>dd</code>]]
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}