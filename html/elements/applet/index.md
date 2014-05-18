{{Page_Title|applet -- obsolete}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|Deprecated}}
{{API_Name|applet}}
{{Summary_Section|The '''applet''' element (&lt;applet&gt;) embeds a Java applet into a web page.}}
{{Markup_Element
|DOM_interface=dom/HTMLAppletElement
|Content=The '''applet''' element has been deprecated with HTML 4.01 and made ''obsolete'' with HTML5.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following example shows how to embed Java applet 'myApplet' into a web page.
|Code=<applet code="myApplet.class" width="500" height="500">
My Java applet goes here! 
</applet>
}}
}}
{{Notes_Section
|Notes====Remarks===
To use executable content specified by the '''applet''' element, a user's computer must have  a Java Runtime Environment (JRE) solution installed.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/REC-html40/struct/objects.html#h-13.4
|Status=W3C Recommendation
|Relevant_changes=Feature marked as deprecated
}}{{Related Specification
|Name=HTML5
|URL=http://www.w3.org/TR/html5/obsolete.html#the-applet-element
|Status=W3C Candidate Recommendation
|Relevant_changes=Feature marked as obsolete
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=8+
|Note=Windows Internet Explorer 8 and later. The value of the [[html/attributes/codeBase|'''codeBase''']] attribute depends on the current document compatibility mode.
}}
}}
{{See_Also_Section}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}