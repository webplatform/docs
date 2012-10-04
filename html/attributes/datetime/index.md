{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Topics|HTML}}
{{Notes_Section
|Notes=
===Remarks===
The following is the standard format for defining the time and date as defined in HTML 4.0 (and taken from the ISO reference 8601:1988).
{| class="wikitable"
|-
!Standard Date-Time Format
|-
|YYYY-MM-DDThh:mm:ssTZD
|}
 
The following table shows the datetime syntax.
{| class="wikitable"
|-
!Syntax
!Definition
|-
|YYYY
|Four-digit year
|-
|MM
|Two-digit month (such as: 01{{=}}January)
|-
|DD
|Two-digit day of month (01 through 31)
|-
|hh
|Two-digit hour (00 through 23) (A.M./P.M. not allowed)
|-
|mm
|Two-digit minute (00 through 59)
|-
|ss
|Two-digit second (00 through 59)
|-
|TZD
|Time zone designator
|}
 
The following table shows  values for the Time Zone Designator(TZD) above.
{| class="wikitable"
|-
!TZD syntax
!Definition
|-
|''Z''
|(Must be uppercase) Specifies Coordinated Universal Time (UTC)
|-
|''+hh:mm''
|Specified time is hh hours and mm minutes ahead of UTC.
|-
|''-hh:mm''
|Specified time is is hh hours and mm minutes behind UTC.
|}
 
If a generating application does not know the time to the second, it may use the value "00" for the seconds (and minutes and hours if necessary).
The standard specifies an uppercase "T" to indicate the beginning of the time element.
'''Note'''   This standard does not address the issue of leap seconds.
There is no functionality implemented for this property unless defined by the author.
'''dateTime''' was introduced in Microsoft Internet Explorer 6
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>ins</code>
*<code>del</code>
|Topic_clusters=html
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}