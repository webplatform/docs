{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info


|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the '''input type{{=}}text''' element to create an empty text control that can contain 15 characters without requiring the user to scroll to read all of the text.
|Code=&lt;INPUT TYPE{{=}}text VALUE{{=}}"" NAME{{=}}"textbox" SIZE{{=}}15&gt;
}}{{Single Example
|Description=This example uses script to detect the content of the text box and display it in a dialog box.
|Code=&lt;SCRIPT&gt;
function detectEntry()
{
    alert("Your name is " + textbox.value)
}
&lt;/SCRIPT&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
The purpose of the '''value''' property depends on the type of control as described in the following table.
{| class="wikitable"
|-
|'''input type{{=}}checkbox'''
|The selected value. The control submits this value only if the user has selected the control. Otherwise, the control submits no value.
|-
|'''input type{{=}}file'''
|The value, a file name, typed by the user into the control. Unlike other controls, this value is read-only.
|-
|'''input type{{=}}hidden'''
|The value that the control submits when the form is submitted.
|-
|'''input type{{=}}password'''
|The default value. The control displays this value when it is first created and when the user clicks the reset button.
|-
|'''input type{{=}}radio'''
|The selected value. The control submits this value only if the user has selected the control. Otherwise, the control submits no value.
|-
|'''input type{{=}}reset'''
|The button label. If not set, the label defaults to Reset.
|-
|'''input type{{=}}submit'''
|The button label. If not set, the label defaults to Submit.
|-
|'''input type{{=}}text'''
|The default value. The control displays this value when it is first created and when the user clicks the reset button.
|}
 
The [[dom/properties/value (type/file) B685|'''value''']] property of the '''input type{{=}}file''' object returns only the file name and not the path of the file to machines outside the local machine security zone. For more information on security zones, see About URL Security Zones.
The initial setting of the '''value''' property is the initial display value for the control object.
The user may edit the '''value''' text prior to submission of a control object's content.  If the control object is reset using the '''input type{{=}}reset''' control object, the initial value is restored.
The '''value'''  property text of the '''input type{{=}}password''' object is always displayed with each character's text hidden, such as with an asterisk (*) placeholder.
'''Note'''  Though the '''input type{{=}}password''' '''value''' property display text is hidden, data is passed to the server in clear text, and may be read by anyone with access to the network.
'''Note'''  Though the display text is hidden, data is passed to the server in clear text, and may be read by anyone with access to the network.
|Import_Notes====Syntax===
===Standards information===
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
*<code>input</code>
*<code>input type{{=}}checkbox</code>
*<code>input type{{=}}password</code>
*<code>input type{{=}}text</code>
*<code>input type{{=}}file</code>
*<code>input type{{=}}hidden</code>
*<code>input type{{=}}button</code>
*<code>input type{{=}}radio</code>
*<code>input type{{=}}reset</code>
*<code>input type{{=}}submit</code>
*<code>[[html/elements/input/type/range|input type{{=}}range]]</code>
*<code>[[html/elements/input/type/number|input type{{=}}number]]</code>
*<code>[[html/elements/input/type/email|input type{{=}}email]]</code>
*<code>[[html/elements/input/type/url|input type{{=}}url]]</code>
*<code>[[html/elements/input/type/tel|input type{{=}}tel]]</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}