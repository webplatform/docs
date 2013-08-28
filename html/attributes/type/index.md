{{Page_Title|type}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=Yes
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
|Content=The type attribute specifies the type of <input> element to display.

The default type is: text.

Tip: This is not a required attribute, but we think you should always include it.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Code=<form action="demo_form.asp">
Username: <input type="text" name="usrname"><br>
<input type="submit" value="Submit">
</form>
}}
}}
{{Notes_Section
|Notes====Remarks===
Only the '''type''' property is writeable.
The '''type''' property is read/write-once, but only when an '''input''' element is created with the [[dom/methods/createElement|'''createElement''']] method and before it is added to the document.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 4.10.7
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 2.5.5
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 17.4
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
*<code>[[dom/HTMLInputElement|HTMLInputElement]]</code>
*<code>input type{{=}}button</code>
*<code>input type{{=}}checkbox</code>
*<code>[[html/elements/input/type/email|input type{{=}}email]]</code>
*<code>input type{{=}}file</code>
*<code>input type{{=}}hidden</code>
*<code>input type{{=}}image</code>
*<code>[[html/elements/input/type/number|input type{{=}}number]]</code>
*<code>input type{{=}}password</code>
*<code>[[html/elements/input/type/range|input type{{=}}range]]</code>
*<code>input type{{=}}radio</code>
*<code>input type{{=}}reset</code>
*<code>[[html/elements/input/type/search|input type{{=}}search]]</code>
*<code>input type{{=}}submit</code>
*<code>[[html/elements/input/type/tel|input type{{=}}tel]]</code>
*<code>input type{{=}}text</code>
*<code>[[html/elements/input/type/url|input type{{=}}url]]</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}