{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The element's custom validity message has been set to a non-empty string by calling the element's setCustomValidity() method.}}
{{API_Object_Property
|Property_applies_to=dom/ValidityState
|Read_only=Yes
|Example_object_name=element.validity
|Return_value_name=hasErrorStatus
|Javascript_data_type=Boolean
|Return_value_description=Whether the element has raised a custom error.
|Example_value_name=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=var elem {{=}} document.getElementById('email_addr_confirm');
elem.addEventListener('blur', verifyEmail);

function verifyEmail(evt) {
  var emlcfm{{=}} evt.srcElement;
  var eml{{=}}document.getElementById('email_addr');
  if (emlcfm.value !{{=}} eml.value) {
    // the provided value doesn’t match the primary email address
    emlcfm.setCustomValidity('The two email addresses must match.');
// the emlcfm.validity.customError is true;
  } else {
    // input is valid -- reset the error state, has to be an empty string
    <pre>emlcfm.setCustomValidity('');</pre>
// the emlcfm.validity.customError is false;
  }
}
|LiveURL=
}}
}}
{{Notes_Section
|Usage=HTML5 Web form validation
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C HTML5
|URL=http://www.w3.org/TR/html5/
|Status=Working Draft
|Relevant_changes=Section 4.10.21.3
}}{{Related Specification
|Name=WHATWG HTML
|URL=http://www.whatwg.org/specs/web-apps/current-work/multipage
|Status=Living Standard
|Relevant_changes=Section 4.10.21.3
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN, HTML5Rocks
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh773352(v=vs.85).aspx customError Property]
|HTML5Rocks_link=[http://www.html5rocks.com/en/tutorials/forms/html5forms/ Making forms fabulous]
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}