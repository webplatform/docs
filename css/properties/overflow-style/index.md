{{Page_Title}}
{{Flags
|Content=Compatibility Incomplete
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Specifies the preferred scrolling methods for elements that overflow.}}
{{CSS Property
|Initial value=auto
|Applies to=non-replaced block-level elements and non-replaced inline-block elements
|Inherited=Yes
|Media=interactive
|Computed value=as specified
|Animatable=No
|CSS object model property=overflowStyle
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=auto
|Description=Initial value. Indicates no preference.
}}{{CSS Property Value
|Data Type=none
|Description=Indicates the element does not display any scrolling mechanism, even when its content overflows. 

Unlike [[css/properties/overflow|'''overflow''']]: '''hidden''', elements with '''overflow-style''': '''none''' can still be scrolled via touch panning, keyboard, or mouse wheel.
}}{{CSS Property Value
|Data Type=scrollbar
|Description=Indicates the element displays a classic scrollbar-type control when its content overflows.  

Scrollbars do not overlay content, and therefore take up extra layout space along the edges of the element where they appear.
}}{{CSS Property Value
|Data Type=panner
|Description=A panner is typically a rectangle shown in one corner of the element, with a smaller rectangle inside. The larger rectangle represents all the available content of the element and the smaller one the visible part. The smaller rectangle can be moved around by the user to move the content of the element accordingly.
}}{{CSS Property Value
|Data Type=move
|Description=The value ‘move’ refers to a method where the user can move the content of the element directly (rather than indirectly by moving a scrollbar or a panner). Typically, the mouse pointer changes into a hand or a cross of four arrows to indicate that the user can drag the content around with the mouse. Sometimes the user needs to explicitly activate the move mode and in that case he often can use both dragging (with the mouse) and key events to move the content.
}}{{CSS Property Value
|Data Type=marquee
|Description=The marquee effect (value ‘marquee’) consists of the content moving autonomously, without any user events to control it. A user who waits long enough will eventually see all the content that overflows.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/* Top preference for a scrolling mechanism is a panner. 
   If not available no visible scrolling mechanism should be displayed */
overflow-style: panner, none;
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''overflow-style''' property only has an effect on elements that overflow using the [[css/properties/overflow|'''overflow''']] property.
When using auto-hiding scrollbars, you should ensure your content has sufficient padding to prevent interactive content from being obscured beneath the scrollbar.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Basic Box Model
|URL=http://www.w3.org/TR/css3-box/#the-lsquo3
|Status=W3C Working Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Note=In Internet Explorer for the desktop, on the root element, '''auto''' behaves like '''scrollbar'''.  In Internet Explorer, on the root element, '''auto''' behaves like '''-ms-autohiding-scrollbar'''.
}}
}}
{{See_Also_Section
|Topic_clusters=Box Model, Touch
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}