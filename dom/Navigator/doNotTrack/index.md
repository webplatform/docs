{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=MSDN documentation needs updating
ref to the latest draft.
navigator.msdoNotTracked dropped in favor of request headers.
A screen shot of the Blocked content Icon in the IE address bar would be helpful.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Returns the user's do-not-track setting. This is "yes" if the user has requested not to be tracked by web sites, content, or advertising.}}
{{API_Object_Property
|Property_applies_to=dom/Navigator
|Read_only=Yes
|Example_object_name=navigator
|Return_value_description=Note that navigator.doNotTrack is not the value sent for the do-not-track header.  When the do-not-track header sends "1", navigator.doNotTrack is "yes".  When the header is unset, navigator.doNotTrack is "unspecified".  When the header sends "0" (currently unsupported in Firefox), navigator.doNotTrack is "no".
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Usage=Could be used to determine if the client web browser may be blocking some page content.

In MSIE browsers when ActiveX content or other content is blocked an Icon is displayed in the Address bar which the user can click to disable Tracking Protection and/or ActiveX filtering for the current site.
|Notes=IE9 uses a vendor prefix, eg.  navigator.msDoNotTrack

IE9, Opera 12, Safari 5.1, and Chrome 31 are based on an earlier version of this specification where navigator.doNotTrack is the value sent for the do-not-track header.

IE10 and higher do not use the doNotTrack header which is user configured from the Advanced tab of Internet Options. There is no navigator.doNotTrack or navigator.msdoNotTrack property in those MSIE versions.
|Import_Notes====Standards information===
The current [http://www.w3.org/TR/tracking-dnt/ Tracking Preference Expression] (Working Draft) is based on an earlier version of this specification where navigator.doNotTrack is the value sent for the do-not-track header.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[http://go.microsoft.com/fwlink/p/?LinkId{{=}}212756 Internet Explorer Blog: Introducing Tracking Protection]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/navigator.doNotTrack navigator.doNotTrack]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/gg699483(v=vs.85).aspx navigator.msDoNotTrack]
|HTML5Rocks_link=
}}