{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The 'transition-duration' property specifies the length of time a transition animation takes to complete.}}
{{CSS Property
|Initial value=0s
|Applies to=all elements, :before and :after pseudo elements
|Inherited=No
|Media=interactive
|Computed value=Same as specified value
|Animatable=No
|CSS object model property=N/A
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=time
|Description=Floating-point number, followed by a time units designator (<code>ms</code> or <code>s</code>). For more information about the supported time units, see '''CSS Values and Units Reference'''.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/*
  * This example gradually changes the background color
  * of a div to red over the specified duration time(3s)
  */
div:hover{
	background-color: red;
	transition-duration:3s;
}
|LiveURL=http://code.webplatform.org/gist/5842067
}}
}}
{{Notes_Section
|Notes=Transitions respect Cascading Style Sheets (CSS) box model constraints such as [[css/properties/min-width|'''min-width''']].
For example, if an element is declared with a [[css/properties/min-width|'''min-width''']] value of <code>50px</code> then a transition to a width of <code>25px</code> is not valid. In a case such as this, the transition runs for the specified duration from the start value until a valid maximum or minimum end value, as appropriate.
|Import_Notes====Standards information===
*[http://www.w3.org/TR/css3-transitions/#transition-duration-property CSS Transitions Module Level 3], Section 2.2
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=22.0
|Firefox_supported=Yes
|Firefox_version=16.0
|Firefox_prefixed_supported=Yes
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Yes
|Internet_explorer_prefixed_version=10.0
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Yes
|Opera_prefixed_version=12.0
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Yes
|Safari_prefixed_version=5.1
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Transitions
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}