{{Page_Title}}
{{Flags
|Checked_Out=No
|Editorial notes=New listing page with proper object capitalization; replaces '''document'''.
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Document is one of the most important objects in the DOM. It is where a majority of API methods and properties are rooted.}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=if (document.title !{{=}}{{=}} "") {
    console.log("The title is " + document.title)
}
}}{{Single Example
|Language=HTML
|Description=This example shows an event handler function that displays the current position of the mouse, relative to the upper-left corner of the document, in a console window.
|Code=&lt;!doctype html&gt;
&lt;html&gt;
 &lt;head&gt;
  &lt;title&gt;Report mouse moves&lt;/title&gt;
  &lt;script&gt;
    function reportMove()
    {
      console.log("X {{=}} " + window.event.x + ", Y {{=}} " + window.event.y);
    }
  &lt;/script&gt;
 &lt;/head&gt;
 &lt;body onmousemove{{=}}"reportMove()"&gt;  
  &lt;h1&gt;Welcome!&lt;/h1&gt;
 &lt;/body&gt;
&lt;/html&gt;
}}
}}
{{Notes_Section
|Usage=Use the '''document''' object to examine, modify, or add content to an HTML document and to process events within that document. In a script, the '''document''' object can be referenced through the '''document''' property of the '''window''' object or it can be referenced directly.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 2 HTML
|URL=http://www.w3.org/TR/DOM-Level-2-HTML
|Status=Recommendation
|Relevant_changes=Section 1.6.5
}}{{Related Specification
|Name=DOM Level 3 Core
|URL=http://www.w3.org/TR/2004/REC-DOM-Level-3-Core-20040407
|Status=Recommendation
|Relevant_changes=Section 1.4
}}{{Related Specification
|Name=W3C HTML5
|URL=http://www.w3.org/TR/html5/
|Status=Working Draft
|Relevant_changes=Section 3.1.1
}}{{Related Specification
|Name=WHATWG HTML
|URL=http://www.whatwg.org/specs/web-apps/current-work/multipage/
|Status=Living Standard
|Relevant_changes=Section 3.1.1
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}
{{Concept_Listing
|Use_page_title=No
|List_all_subpages=No
}}