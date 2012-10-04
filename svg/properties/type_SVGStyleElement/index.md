{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Notes_Section
|Notes=
===Remarks===
The '''type'''   property  specifies the style sheet language of the [[svg/elements/style|'''style''']] element's contents. The style sheet language is specified as a content type (for example, <code>"text/css"</code>).
If  you do not provide a type, the value of <code>contentStyleType</code> on the [[svg/elements/svg|'''svg''']] element is used, which  defaults to <code>"text/css"</code>. If a [[svg/elements/style|'''style''']] element falls outside of the outermost '''svg''' element and  you do not provide the type, the value of <code>contentStyleType</code> on the '''type''' element defaults to <code>"text/css"</code>.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204734 Scalable Vector Graphics: Styling], Section 6.18.1


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[svg/elements/style|SVGStyleElement]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}