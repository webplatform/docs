{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add Category, Parent, Children and Compatibility information. Delete HTML information sub section.
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The '''form''' element (&lt;form&gt;) defines an HTML form for user input, subsequently to be submitted to a website or service.}}
{{Markup_Element
|DOM_interface=dom/HTMLFormElement
|Tag_omissions=Closing tag required
|CSS_display=block
|Content====Common Attributes===

{{{!}}
! Name
! Value
! Purpose
! Example
! Validity
{{!}}-
{{!}} [[html/attributes/accept-charset|'''accept-charset''']]
{{!}}
{{!}}
{{!}}
{{!}}
{{!}}-
{{!}} [[html/attributes/action |'''action''']]
{{!}}
{{!}}
{{!}}
{{!}}
{{!}}-
{{!}} [[html/attributes/autocomplete|'''autocomplete''']]
{{!}}
{{!}}
{{!}}
{{!}}
{{!}}-
{{!}} [[html/attributes/method|'''method''']]
{{!}}
{{!}}
{{!}}
{{!}}
{{!}}-
{{!}} [[html/attributes/name|'''name''']]
{{!}}
{{!}}
{{!}}
{{!}}
{{!}}-
{{!}} [[html/attributes/novalidate|'''novalidate''']]
{{!}}
{{!}}
{{!}}
{{!}}
{{!}}-
{{!}} [[html/attributes/target|'''target''']]
{{!}}
{{!}}
{{!}}
{{!}}
{{!}}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''form''' element to create a basic form containing a text entry box for the user's name and a select control for choosing a favorite ice cream flavor. When the user clicks the '''Submit''' button, the form sends the data to the URL listed in the [[html/attributes/action|'''action''']] attribute. The value of the [[html/attributes/method|'''method''']] attribute determines how to send the data to the server.
|Code=<nowiki>
    <form action="http://example.microsoft.com/sample.asp" method="post">
        Enter your name: <input name="FName"/><br/>
        Favorite Ice Cream Flavor:
        <select name="Flavor">
            <option value="Chocolate">Chocolate</option>
            <option value="Strawberry">Strawberry</option>
            <option value="Vanilla" selected="selected">Vanilla</option>
        </select>
        <p><input type="submit"/></p>
    </form>
</nowiki>
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
'''Security Warning:  '''Using this object incorrectly can compromise the security of your application. Data submitted through a form using the HTTP protocol is not encrypted and can be read and possibly tampered with in transmission. The Secure Hypertext Transfer Protocol (HTTPS) can provide more secure data transmission. You should review the Security Considerations: Dynamic HTML before continuing.
Forms enable client-side users to submit data to a server in a standardized format. The creator of a '''form''' designs it to collect the required data using a variety of controls, such as '''input''' or '''select'''. Users viewing the '''form''' fill in the data and then click the '''Submit''' button to send the data to the server. A script on the server then processes the data.
Each control element's [[html/attributes/name (frames)|'''name''']] attribute must be defined if the data is to be submitted with the form. An element in a form can be referenced by the '''name''' property or the [[html/attributes/id|'''id''']] property, or through the [[dom/properties/elements|'''elements''']] collection.
When the focus is on a control in a form and the user presses ESC, the value of the control reverts to the last value. The form resets if the user presses ESC again.
If the form includes only one text box and the user presses ENTER, the [[dom/events/submit|'''onsubmit''']] event fires. If the form has an '''input type="submit"''' element, it will appear as a button with a dark border, which indicates the user can press ENTER to submit the form.
Windows Internet Explorer 8 and later. The value of the [[html/attributes/action|'''action''']] attribute depends on the current document compatibility mode.  In addition, the '''form object''' now supports [[html/attributes/enctype|'''enctype''']] as a DOM attribute.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/forms.html#the-form-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/forms.html#the-form-element
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/interact/forms.html#edef-FORM
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections====Related pages (MSDN)===
*<code>[http://msdn.microsoft.com/en-us/library/ms971057.aspx 1,001 Ways to Get Input from Web Users]</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}



}





}