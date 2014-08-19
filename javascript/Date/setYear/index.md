{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Obsolete; deletion candidate
|Checked_Out=No
}}
{{Summary_Section|Sets the year value in the Date object.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=dateObj.'''setYear(''' numYear ''')'''
}}
|Values={{JS Syntax Parameter
|Name=dateObj
|Required=Required
|Description=Any Date object.
}}{{JS Syntax Parameter
|Name=numYear
|Required=Required
|Description=For the years 1900 through 1999, this is a numeric value equal to the year minus 1900. For dates outside that range, this is a 4-digit numeric value.
}}
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Remarks_Section
|Remarks=This method is obsolete, and is maintained for backwards compatibility only. Use the '''setFullYear''' method instead.

To set the year of a Date object to 1997, call '''setYear(97)'''. To set the year to 2010, call '''setYear(2010)'''. Finally, to set the year to a year in the range 0-99, use the '''setFullYear''' method.

'''Note''' -- For JavaScript version 1.0, '''setYear''' uses a value that is the result of the addition of 1900 to the year value provided by numYear , regardless of the value of the year. For example, to set the year to 1899 numYear is -1 and to set the year 2000 numYear is 100.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getFullYear{{!}}getFullYear Method (Date)]]
* [[javascript/Date/getUTCFullYear{{!}}getUTCFullYear Method (Date)]]
* [[javascript/Date/getYear{{!}}getYear Method (Date)]]
* [[javascript/Date/setFullYear{{!}}setFullYear Method (Date)]]
* [[javascript/Date/setUTCFullYear{{!}}setUTCFullYear Method (Date)]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/0f0shhbs(v=vs.94).aspx
|HTML5Rocks_link=
}}