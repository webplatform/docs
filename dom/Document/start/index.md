{{Page_Title}}
{{Flags
|High-level issues=Deletion Candidate, Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
|Editorial notes={{Editorial/Deletion_Candidate
| Content has no standard and is only for a deprecated element (marquee.) No real use being documented now or in the future since it isn't on any track to be a standard.
}}
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section}}
{{Event
|Event_applies_to=dom/Document
|Synchronous=No
|Bubbles=No
|Target=dom/Element
|Cancelable=No
|Interface=dom/Document
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example shows how to use the '''onstart''' event on a '''marquee'''.
|Code=&lt;BODY&gt;
&lt;P&gt;An alert dialog box displays each time the onstart event fires.
&lt;MARQUEE onstart{{=}}"alert('onstart fired')"
		 BEHAVIOR{{=}}alernate LOOP{{=}}2&gt;Marquee Text&lt;/MARQUEE&gt;
&lt;/BODY&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onstartEX.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''start''' method does not cause the '''onstart''' event to fire.
Initiates the next loop of the '''marquee''' contents.
To invoke this event, do one of the following:
*Set the [[html/attributes/loop|'''LOOP''']] attribute to 1 or higher.
*Omit the [[html/attributes/loop|'''LOOP''']] attribute so that the '''marquee''' loops indefinitely.

The ''pEvtObj'' parameter is required for the following interfaces:
*'''HTMLAnchorEvents2'''
*'''HTMLAreaEvents2'''
*'''HTMLButtonElementEvents2'''
*'''HTMLControlElementEvents2'''
*'''HTMLDocumentEvents2'''
*'''HTMLElementEvents2'''
*'''HTMLFormElementEvents2'''
*'''HTMLImgEvents2'''
*'''HTMLFrameSiteEvents2'''
*'''HTMLInputFileElementEvents2'''
*'''HTMLInputImageEvents2'''
*'''HTMLInputTextElementEvents2'''
*'''HTMLLabelEvents2'''
*'''HTMLLinkElementEvents2'''
*'''HTMLMapEvents2'''
*'''HTMLMarqueeElementEvents2'''
*'''HTMLObjectElementEvents2'''
*'''HTMLOptionButtonElementEvents2'''
*'''HTMLScriptEvents2'''
*'''HTMLSelectElementEvents2'''
*'''HTMLStyleElementEvents2'''
*'''HTMLTableEvents2'''
*'''HTMLTextContainerEvents2'''
*'''HTMLWindowEvents2'''
|Import_Notes====Syntax===
===Standards information===
There are no standards that apply here.

===Event handler parameters===
;''pEvtObj'' [in]:Type: '''<b>IHTMLEventObj'''</b>
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
|Manual_sections====Related pages (MSDN)===
*<code>marquee</code>
*<code>Reference</code>
*<code>behavior</code>
*<code>[[html/attributes/loop|loop]]</code>
*<code>[[dom/Event/finish|finish]]</code>
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}