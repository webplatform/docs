{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Deletion Candidate: It's deprecated, http://www.w3.org/TR/html5/obsolete.html#non-conforming-features
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Nonstandard. Defines a scrolling area (usually horizontal) of text.}}
{{Markup_Element
|DOM_interface=dom/HTMLMarqueeElement
|Tag_omissions=
|CSS_display=
|Content=No, really. don't use it.
}}
{{Examples_Section
|Not_required=Yes
|Examples={{Single Example
|Language=
|Description=The following example uses the '''MARQUEE''' element to scroll the marquee from left to right across the screen, moving it 10 pixels every 200 milliseconds.
|Code=&lt;MARQUEE DIRECTION{{=}}RIGHT BEHAVIOR{{=}}SCROLL SCROLLAMOUNT{{=}}10 SCROLLDELAY{{=}}200&gt;
This is a scrolling marquee.
&lt;/MARQUEE&gt;
|LiveURL=
}}{{Single Example
|Language=
|Description=The following example shows some uses of the [[dom/properties/scrollLeft|'''scrollLeft''']] and [[dom/properties/scrollTop|'''scrollTop''']] properties with the '''marquee''' element.
|Code=&lt;MARQUEE id{{=}}m1 direction{{=}}right style{{=}}"border-width:2px;border-style:solid;" 
width{{=}}200 height{{=}}200&gt;right&lt;/MARQUEE&gt;&lt;BR&gt;
&lt;!-- Push this button to read the scrollLeft and scrollTop property values 
as the marquee scrolls. --&gt;
&lt;BUTTON onclick{{=}}"alert('scrollLeft: ' + m1.scrollLeft + ' scrollRight: ' + m1.scrollTop)"&gt;
Read&lt;/BUTTON&gt;
&lt;!--When the marquee is stopped, you can set scrollLeft in a horizontal marquee, 
or set scrollTop in a vertical marquee.   --&gt;
&lt;BUTTON onclick{{=}}"m1.stop();m1.scrollLeft {{=}} 190;"&gt;Stop &amp; Set scrollLeft{{=}}190
&lt;/BUTTON&gt;
&lt;BUTTON onclick{{=}}"m1.start();"&gt;Start&lt;/BUTTON&gt;
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
The default width of the '''MARQUEE''' element is equal to the width of its parent element. When a '''MARQUEE''' is in a '''TD''' that does not specify a width, you should explicitly set the width of '''MARQUEE'''. If neither the '''MARQUEE''' nor the '''TD''' has a width specified, the marquee is collapsed to a 1-pixel width.
To create a vertically scrolling '''marquee''', set its [[dom/properties/scrollLeft|'''scrollLeft''']] property to 0. To create a horizontally scrolling marquee, set its [[dom/properties/scrollTop|'''scrollTop''']] property to 0, overriding any script setting.
The [[dom/properties/scrollLeft|'''scrollLeft''']] and [[dom/properties/scrollTop|'''scrollTop''']] properties are read-only while the '''marquee''' is scrolling. When not scrolling, '''scrollLeft''' is read/write for a '''marquee''' set to scroll horizontally and '''scrollTop''' is read/write for a '''marquee''' set to scroll vertically.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
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