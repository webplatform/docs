{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Controls the visible highlighting of selections of text and elements. It is possible to blind out selection completely or to allow the selection of text only.}}
{{CSS Property
|Initial value=all
|Applies to=Visible elements
|Inherited=Yes
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=none
|Description=None of the descendants of the element can be selected, neither text nor images.
}}{{CSS Property Value
|Data Type=text
|Description=Only text of the element and its descendants can be selected.
}}{{CSS Property Value
|Data Type=all
|Description=Default. Everything, text and images, can be selected.
}}{{CSS Property Value
|Data Type=element
|Description=Only specified elements can be selected. Only supported in Firefox and Internet Explorer.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Deactivate selection of text for elements with the class '''none'''.
|Code=.no-select {
    -webkit-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    user-select: none;
}
|LiveURL=http://jsfiddle.net/R5Ygm/
}}
}}
{{Notes_Section
|Usage=Needs vendor prefixes. 
|Notes=Also works on mobile devices to suppress selection by touch and hold.
}}
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
|Topic_clusters=CSS Attributes
|Manual_sections====Related pages (MSDN)===
*<code>[http://go.microsoft.com/fwlink/p/?LinkID{{=}}235901 IE Test Drive: User-Select]</code>
*<code>[https://developer.mozilla.org/en-US/docs/CSS/user-select]</code>
}}
{{Topics|CSS, Design}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
{{CSS_Selector
|Content=
}}