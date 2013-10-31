{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Event
|Interface=dom/Event
|Target=dom/Element
|Default_action=
|Content=
|Event_applies_to=dom/Event
|Synchronous=No
|Bubbles=No
|Cancelable=No
}}
{{Topics|Events}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the '''onbeforeprint''' to make all hidden sections of the document visible just before the document prints. The [[dom/events/afterprint|'''onafterprint''']] event is processed after the document prints to return the document to its original state.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onbeforeprint.htm
|Code=
function window.onbeforeprint()
{
    // Walk through all the elements in the document with
    // CLASS{{=}}"collapsed" and set it to "expanded" just for printing.
   var coll {{=}} document.all.tags("DIV");
   if (coll!{{=}}null)
   {
      for (i{{=}}0; i&lt;coll.length; i++) 
         if (coll[i].className {{=}}{{=}} "collapsed")
         {  
           coll[i].className {{=}} "expanded";
           
        // After printing, make sure to set CLASS{{=}}"collapsed" 
        // only for those that were expanded just for printing.
           coll[i].bExpandedForPrinting {{=}} true;
         }
         else if (coll[i].className {{=}}{{=}} "expanded")
            coll[i].bExpandedForPrinting {{=}} false;
   }
}
function window.onafterprint()
{
   // Walk through all the elements in the doc with CLASS{{=}}"expanded"
   // and set it to "collapsed" if expanded just for 
   // printing.
   var coll {{=}} document.all.tags("DIV");
   if (coll!{{=}}null)
   {
      for (i{{=}}0; i &lt; coll.length; i++) 
         if ((coll[i].className {{=}}{{=}} "expanded") &amp;&amp;
             (coll[i].bExpandedForPrinting))
         {  
           coll[i].className {{=}} "collapsed";
           coll[i].bExpandedForPrinting {{=}} false;
         }
   }
}
}}}}
{{Notes_Section
|Notes=
===Remarks===
Use this event to modify the document just before it prints or previews for printing. In most cases it is used to make all the information on the document visible just before printing.
Use the event in conjunction with the [[dom/events/afterprint|'''onafterprint''']] event to undo the changes made to the document in the '''onbeforeprint''' event.
Prints the document associated with the object for which the event is specified.
To invoke this event, do one of the following:
*Choose Print or Print Preview from the File menu.
*Press CTRL+P.
*Right-click anywhere on a document, and choose Print.
*Right-click a link on a document, and choose Print.
*From Windows Explorer, select an .htm file and choose Print from the File menu.
*From Windows Explorer, right-click an .htm file and choose Print.

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

|Import_Notes=
===Syntax===
===Standards information===
There are no standards that apply here.

===Event handler parameters===
;''pEvtObj'' [in]:Type: '''<b>IHTMLEventObj'''</b>

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>window</code>
*<code>body</code>
*<code>frameSet</code>
*<code>Reference</code>
*<code>[[dom/events/afterprint|onafterprint]]</code>
*<code>print</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}