{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Deletion Candidate: It's deprecated, http://www.w3.org/TR/html5/obsolete.html#non-conforming-features
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Deprecated}}
{{API_Name}}
{{Summary_Section|The '''frameset''' element (&lt;frameset&gt;) defines a collection of frames.
The &lt;frameset&gt; element holds one or more [[html/elements/frame|&lt;frame&gt;]] elements. Each &lt;frame&gt; element can hold a separate document.
The &lt;frameset&gt; tag is obsolete in HTML5.
}}
{{Markup_Element
|DOM_interface=dom/HTMLFrameSetElement
|Tag_omissions=
|CSS_display=
|Content=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=
|Description=This example uses the '''FRAMESET''' element to define three columns of rectangular frames in a document.
|Code=&lt;FRAMESET COLS{{=}}"25%, 50%, *"&gt;
&lt;FRAME SRC{{=}}"contents.htm"&gt;
&lt;FRAME SRC{{=}}"info.htm"&gt;
&lt;FRAME SCROLLING{{=}}"NO" SRC{{=}}"graphic.htm"&gt;
&lt;/FRAMESET&gt;
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
The '''FRAMESET''' element is a container for the '''FRAME''' element. An HTML document can contain either the '''FRAMESET''' element or the '''BODY''' element, but not both.
If a user opens a folder inside a frame and then clicks something in the folder, the file or folder that the user clicks takes over the entire window. For example, suppose that a page contains two frames, one frame pointing to http://www.microsoft.com and the second frame pointing to a network drive. If the user clicks a file or folder in the second frame, that frame takes control of the entire window, including the first frame. For file types that the application cannot host, such as .txt files, a separate window in the appropriate host application is opened.
A folder is a part of the file system hierarchy, but it does not necessarily represent anything in the file system. An example is Network Neighborhood.
'''Security Warning:  '''
To protect user privacy and safeguard your applications, Windows Internet Explorer restricts some interactions between frames that host Web pages from different domains. For more information about using the Dynamic HTML (DHTML) object model with the '''frame''' and '''iframe''' objects, see About Cross-Frame Scripting and Security and Security Considerations: Dynamic HTML.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections====Related pages (MSDN)===
*<code>frame</code>
}}
{{Topics|HTML}}
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
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}