{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Fires when a history entry changes.}}
{{API_Object
|Subclass_of=dom/Event
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=window.onpopstate = function(evt) { document.write("location: " + document.location + ", state: " + JSON.stringify(evt.state)); };
}}
}}
{{Notes_Section
|Usage=Used, for example to prevent back navigation to a login page after the user has already logged in.
|Notes====Remarks===
A pop state event is dispatched to the window object every time the active history entry changes.
To read the current history entry immediately, invoke <code>history.state</code>.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=The History Interface
|URL=http://www.w3.org/TR/html5/browsers.html#the-history-interface
|Status=Recommendation
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
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh772349(v=vs.85).aspx PopStateEvent]
|HTML5Rocks_link=
}}