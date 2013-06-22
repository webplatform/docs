{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The 'transition-delay' property defines when the transition will start. A value of ‘0s’ means the transition will execute as soon as the property is changed. Otherwise, the value specifies an offset from the moment the property is changed, and the transition will delay execution by that offset.}}
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

Values are rounded up to the second decimal place.
Each '''transition-delay''' is paired with a corresponding object property  identified in the [[css/properties/transition-property|'''transition-property''']] property.
If more '''transition-delay''' values are declared than corresponding object properties identified in the [[css/properties/transition-property|'''transition-property''']] property, the excess '''transition-delay''' values are ignored.
If fewer  '''transition-delay''' values are declared than corresponding object properties identified in the [[css/properties/transition-property|'''transition-property''']] property, the list of '''transition-delay''' values is repeated from the beginning until the object properties are exhausted.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/*
 * This example show a transition delay after hovering
 *  over a div for the specified delay time.
 * 
 * In this example the background color will change 
 * to red after hovering over a div for 3 seconds. 
 */

div:hover{
    background-color: red;
    transition-delay: 3s;
}
|LiveURL=http://code.webplatform.org/gist/5841921
}}
}}
{{Notes_Section
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}223140 CSS Transitions Module Level 3], Section 2.4
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
|Chrome_prefixed_version=22
|Firefox_supported=Yes
|Firefox_version=16.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
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