{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Add compatibility, list valid values
|Checked_Out=No
|High-level issues=Stub, Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Examples Needed
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The <code>time</code> tag defines either a time (24 hour clock), or a date in the Gregorian calendar, optionally with a time and a time-zone offset. It does not render differently in any of the major browsers.

This element can be used as a way to encode dates and times in a machine-readable way so that, for example, user agents can offer to add birthday reminders or scheduled events to the user's calendar.
}}
{{Markup_Element
|DOM_interface=dom/HTMLTimeElement
|Tag_omissions=Closing tag required
|CSS_display=inline
|Content=The HTML time element (<time>) represents either time on a 24-hour clock or a precise date in the Gregorian calendar (with optional time and timezone information).

This element is intended to be used presenting dates and times in a machine readable format. This can be helpful for user agents to offer any event scheduling for user's calendar.

== Attributes ==

* <code>datetime</code> =  date or time<br />Specifies the date or time that the element represents.

== Validity ==

The datetime value of a time element is the value of the element's datetime attribute, if it has one, or the element's textContent, if it does not.

The kind of content is limited to various kinds of dates, times, time-zone offsets, and durations, as described below:
*A valid month string
** 2012-03
*A valid date string
** 3012-03-29
*A valid time string
** 15:25
** 15:25:35
*A valid local date and time string
** 2012-03-29T15:25:35
** 2012-03-29 15:25:35
*A valid time-zone offset string
** Z
** 0000
** 00:00
**See more details: [http://www.w3.org/TR/html5/the-time-element.html#datetime-value Datetime value] at HTML5 specification.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Code=<nowiki><p>
On <time datetime="1913-03-12">12 March 1913</time>, the city of Canberra
was officially given its name by Lady Denman, the wife of Governor-General
Lord Denman.
</p></nowiki>
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/text-level-semantics.html#the-time-element
|Status=W3C Working Draft
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/text-level-semantics.html#the-time-element
|Status=W3C Recommendation
}}
}}
{{See_Also_Section
|Topic_clusters=HTML
|External_links=* [https://developer.mozilla.org/en-US/docs/HTML/HTML_Elements/time time page at the Mozilla Developer Network].
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=No
|Chrome_version=
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=22.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Unknown
|Android_version=
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=22.0
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Unknown
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}