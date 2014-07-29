{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=but.... example does not work in MSIE.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Gets additional, developer defined, information about an event.}}
{{API_Object_Property
|Property_applies_to=dom/UIEvent
|Read_only=Yes
|Example_object_name=event
|Return_value_name=eventDetails
|Javascript_data_type=Number
|Return_value_description=Returns additional numerical information about the event, depending on the type of event.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Code=&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;head&gt;
  &lt;title&gt;event.detail example&lt;/title&gt;
  &lt;script type{{=}}"text/javascript"&gt;
  function giveDetails(e) {
      var text {{=}} document.getElementById("t");
      text.value {{=}} e.detail;
  }
  function init() {
      var b1 {{=}} document.getElementById("b");
      b1.onclick {{=}} giveDetails;   
  }
  &lt;/script&gt;
&lt;/head&gt;
&lt;body onload="init();"&gt;
&lt;form&gt;
 &lt;input id="b" type="button" value="details"/&gt;
 &lt;input id="t" type="text" value=""/&gt;&lt;br/&gt;
 &lt;input type="reset"/&gt;
&lt;/form&gt;
&lt;/body&gt;
&lt;/html&gt;

}}
}}
{{Notes_Section
|Usage=Use this property to get developer defined information about a developer generated event, if any. When part of a user agent initiated [[dom/UIEvent|UIEvent]], this property is never set.
|Notes=You can set the '''detail'''  property of  an  event  by using the  [[dom/UIEvent/initUIEvent|'''initUIEvent''']] method.

For mouse events, such as click, dblclick, mousedown, or mouseup, the detail property indicates how many times the mouse has been clicked in the same location for this event.

For a dblclick event the value of detail is always 2.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 3 Events
|URL=http://www.w3.org/TR/DOM-Level-3-Events/
|Status=Working Draft
|Relevant_changes=Section 5.2.1
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
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/event.detail event.detail]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff974802(v=vs.85).aspx detail Property]
|HTML5Rocks_link=
}}