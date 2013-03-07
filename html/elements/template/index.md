{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Templates allow you to declare fragments of markup which are parsed as HTML, go unused at page load, but can be instantiated later on at runtime.}}
{{Markup_Element
|DOM_interface=dom/HTMLTemplateElement
|Content=The content of a <code><template></code> element is a hidden portion of the DOM and does not render on page load: scripts don't run, text or images don't display, audio doesn't play, and so forth. Neither are the child nodes of the <code><template></code> accessible with the JavaScript <code>getElementbyId()</code> or <code>querySelector()</code> methods.

Templates can be placed anywhere inside of the <code><head></code>, <code><body></code>, and <code><frameset></code> elements; It can also be used as a child of a <code>&lt;table&gt;</code> or a <code><select></code> element.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description====Basic example===
|Code=<syntaxhighlight>
<table>
<tr>
  <template id="cells-to-repeat">
    <td>some content</td>
  </template>
</tr>
</table>
</syntaxhighlight>
}}{{Single Example
|Language=JavaScript
|Description=To use a template, you need to activate it. Otherwise its content will not render. The simplest way to do this is by creating a deep copy of its <code>.content </code>using <code>cloneNode()</code>. The <code>.content</code> property is read-only and references a <code>DocumentFragment</code> containing the guts of a template.
|Code=var t = document.querySelector('#mytemplate');
t.content.querySelector('img').src = 'logo.png'; // Populate the src at runtime.
document.body.appendChild(t.content.cloneNode(true));
}}
}}
{{Notes_Section
|Notes=* If you're using [https://code.google.com/p/modpagespeed/ modpagespeed], be careful of this [http://code.google.com/p/modpagespeed/issues/detail?id=625 bug]. Templates that define inline <code><style scoped></code>, many be moved to the <code>head</code> with PageSpeed's CSS rewriting rules.
* There's no way to "prerender" a template, meaning you cannot preload assets, process JS, download initial CSS, etc. That goes for both server and client. The only time a template renders is when it goes live.
* Be careful with nested templates. They don't behave as you might expect, and nested templates must be activated separately.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=26
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Unknown
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Web Components
|External_links=* [http://www.html5rocks.com/en/tutorials/webcomponents/template/ HTML's New Template Tag]
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=HTML5Rocks
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=http://www.html5rocks.com/en/tutorials/webcomponents/template/
}}