{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs summary, specs, and compat
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Event
|Event_applies_to=dom/Event
|Synchronous=No
|Bubbles=No
|Target=dom/Element
|Cancelable=No
|Interface=dom/Event
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the '''onafterprint''' event to return the document to its pre-print state. In this case, because the [[dom/Event/beforeprint|'''onbeforeprint''']] event handler makes all currently hidden sections of the document visible for printing, the '''onafterprint''' event sets those sections back to hidden.
|Code=function window.onafterprint()
{
    // Walk through all the elements in the doc with CLASS{{=}}"expanded"
    // and set it to "collapsed" if expanded just for 
    // printing.
   var coll {{=}} document.all.tags("DIV");
   if (coll!{{=}}null)
   {
      for (i{{=}}0; i&lt;coll.length; i++) 
	     if ((coll[i].className {{=}}{{=}} "expanded") &amp;&amp;
		     (coll[i].bExpandedForPrinting))
		 {  
		   coll[i].className {{=}} "collapsed";
		   coll[i].bExpandedForPrinting {{=}} false;
		 }
   }
}
function window.onbeforeprint()
{
    // Walk through all the elements in the doc with CLASS{{=}}"collapsed"
    // and set it to "expanded" just for printing.
   var coll {{=}} document.all.tags("DIV");
   if (coll!{{=}}null)
   {
      for (i{{=}}0; i&lt;coll.length; i++) 
	     if (coll[i].className {{=}}{{=}} "collapsed")
		 {  
		   coll[i].className {{=}} "expanded";
		   
		// After printing, make sure to set
		// CLASS{{=}}"collapsed" only for those that were
		// expanded just for printing.
		   coll[i].bExpandedForPrinting {{=}} true;
		 }
		 else if (coll[i].className {{=}}{{=}} "expanded")
		    coll[i].bExpandedForPrinting {{=}} false;
   }
}
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onbeforeprint.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
This event is usually used with the [[dom/Event/beforeprint|'''onbeforeprint''']] event. Use the '''onbeforeprint''' event to make changes to the document just before it prints or previews for printing. Use the '''onafterprint''' event to undo those changes, reverting the document back to its pre-print or pre-preview state.

To invoke this event, do one of the following:
*Choose Print or Print Preview from the File menu.
*Press CTRL+P.
*Right-click anywhere on a document, and choose Print.
*Right-click a link on a document, and choose Print.
*From Windows Explorer, select an .htm file, and then choose Print from the File menu.
*From Windows Explorer, right-click an .htm file, and then choose Print.

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
*<code>window</code>
*<code>body</code>
*<code>frameSet</code>
*<code>Reference</code>
*<code>[[dom/Event/beforeprint|onbeforeprint]]</code>
*<code>print</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}