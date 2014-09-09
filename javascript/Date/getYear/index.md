{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Obsolete; deletion candidate
|Checked_Out=No
}}
{{Summary_Section|Gets the year of a '''Date''' object.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=dateObj.getYear()
}}
|Values={{JS Syntax Parameter
|Name=
|Required=
|Description=The required dateObj reference is a Date object.
}}
}}
{{JS_Return_Value
|Description=Returns the year.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Remarks_Section
|Remarks='''Important''' -- This method is obsolete, and is provided for backward compatibility only. Use the '''getFullYear''' method instead.

In Internet Explorer 3.0, and then in Internet Explorer versions starting with Internet Explorer 9 standards mode, the value returned is the stored year minus 1900. For example, the year 1899 is returned as -1 and the year 2000 is returned as 100.

In Internet Explorer 4.0 through Internet Explorer 8 standards mode, the formula depends on the year. For the years 1900 through 1999, the value returned is a 2-digit value that is the stored year minus 1900. For dates outside that range, the 4-digit year is returned. For example, 1996 is returned as 96, but 1825 and 2025 are returned as is.
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Date/getFullYear{{!}}getFullYear Method (Date)]]
* [[javascript/Date/getUTCFullYear{{!}}getUTCFullYear Method (Date)]]
* [[javascript/Date/setFullYear{{!}}setFullYear Method (Date)]]
* [[javascript/Date/setUTCFullYear{{!}}setUTCFullYear Method (Date)]]
* [[javascript/Date/setYear{{!}}setYear Method (Date)]]
|External_links=
|Manual_sections=
}}
{{JS Topics
|JS Page Type=JS Method
|Applies to=Date
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/x0a9sc10(v=vs.94).aspx
|HTML5Rocks_link=
}}