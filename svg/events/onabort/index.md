{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs summary, spec reference, standardization status
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Event
|Event_applies_to=dom/Element
|Synchronous=No
|Bubbles=No
|Target=dom/Element
|Cancelable=No
|Interface=dom/objects/Event
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following code example shows how to  handle  the '''onabort''' event.
|Code=<syntaxhighlight lang="xml">
<?xml version="1.0" standalone="no"?>
<!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN"
"http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">
<svg id="outerSvgElement" width="600px" height="210px" version="1.1" xmlns="http://www.w3.org/2000/svg"
     xmlns:xlink="http://www.w3.org/1999/xlink"> <!-- Required for xlink usage. -->
  <script type="application/ecmascript">
    function handleAbortEvent(evt) {
      // Handle the abort event here.
    }

    window.onload = function() {
      var e = document.documentElement; // Root element is svg

      /*
        For the svg element, add an event listener for the onabort event.
        addEventListener parameters: event type, event listener pointer, 'false' = bubbling.
      */
      e.addEventListener('SVGAbort', handleAbortEvent, false);
    }
  </script>
</svg>
</syntaxhighlight>
}}
}}
{{Notes_Section
|Notes====Remarks===

The '''onabort''' event occurs when page loading is stopped before an element  is  loaded  completely.
The target of the event is the [[svg/elements/svg|'''svg''']] element.
The designated element stops loading.
To invoke this event, do one of the following:
*The user presses the browser's stop button before the element  is  loaded  completely.
|Import_Notes====Syntax===

===Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204745 Scalable Vector Graphics: Scripting], Section 18.4.3

===Event handler parameters===

;''pEvt'' [in]:Type: '''IDOMUIEvent'''The [[dom/objects/Event|'''IDOMEvent''']] object.
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

*[[svg/elements/svg|'''SVGSVGElement''']]
*[[dom/events/abort|'''onabort''']]
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}