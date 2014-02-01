{{Page_Title}}
{{Flags}}
{{Summary_Section|Gets the difference in minutes between the time on the local computer and Universal Coordinated Time (UTC).

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= dateObj.getTimezoneOffset() }}
|Values={{JS_Syntax_Parameter
|Name=
|Required=
|Description=The required dateObj reference is a Date object.}}
}}
{{JS_Return_Value
|Description=Returns the number of minutes between the time on the current computer (either the client machine or, if this method is called from a server script, the server machine) and UTC. It is positive if the current computer's local time is behind UTC (e.g., Pacific Daylight Time), and negative if the current computer's local time is ahead of UTC (e.g., Japan). If a server in New York City is contacted by a client in Los Angeles on December 1, '''getTimezoneOffset''' returns 480 if executed on the client, or 300 if executed on the server.}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example shows how to use the '''getTimezoneOffset''' method.

|Code= var date =  new Date();
 var minutes = date.getTimezoneOffset();
 
 if (minutes &lt; 0)
     document.write(minutes / 60 + " hours after UTC");
 else
     document.write(minutes / 60 + " hours before UTC");
 
 // Output (for example, where local time is PST): 
 7 hours before UTC
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getTime{{!}}getTime Method (Date)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/014ykh71(v=vs.94).aspx
|HTML5Rocks_link=
}}