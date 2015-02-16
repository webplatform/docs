{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add Compatibility 
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The '''kbd'' element denotes user input. Typically this is keyboard input (hence "kbd"), but it may also be used to represent other user input, e.g. voice commands or gestures.}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the <code>kbd</code> element to convey a command line command to the user.
|Code=&lt;p&gt;Type the command &lt;kbd&gt;git status&lt;/kbd&gt;
to see the working tree status.&lt;/p&gt;
}}{{Single Example
|Language=HTML
|Description=This example illustrates using <code>kbd</code> to indicate keystrokes.
|Code=&lt;p&gt;Press &lt;kbd&gt;&lt;kbd&gt;Ctrl&lt;/kbd&gt;+&lt;kbd&gt;s&lt;/kbd&gt;&lt;/kbd&gt;
to save your document.&lt;/p&gt;
}}
}}
{{Notes_Section
|Usage=The '''kbd''' element is a phrasing-level element. It must not contain block-level elements, but it can contain other phrasing-level elements.
|Notes=When the '''kbd''' element is nested inside a [[html/elements/samp|'''samp''' element]], it represents the input as it was echoed by the system.

When the '''kbd''' element contains a [[html/elements/samp|'''samp''' element]], it represents input based on system output, for example invoking a menu item.

When the '''kbd''' element is nested inside another '''kbd''' element, it represents an actual key or other single unit of input as appropriate for the input mechanism (see Example 2).
}}
{{Related_Specifications_Section
|Specifications={{Related_Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/text-level-semantics.html#the-kbd-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related_Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/text-level-semantics.html#the-kbd-element
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related_Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/text.html#edef-KBD
|Status=W3C Recommendation
|Relevant_changes=
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
|Topic_clusters=HTML, Text
}}
{{Topics|HTML, XHTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}