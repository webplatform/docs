{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Returns whether the input field value is not the correct syntax.}}
{{API_Object_Property
|Property_applies_to=dom/ValidityState
|Read_only=Yes
|Example_object_name=element.validity
|Return_value_name=result
|Javascript_data_type=Boolean
|Return_value_description=Whether a value is not the correct syntax.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=In the following example validity.typeMismatch is used to validate an email address field instead of a regular expression pattern.
|Code=&lt;!DOCTYPE html&gt;
&lt;html&gt;&lt;head&gt;
&lt;meta http-equiv{{=}}"Content-Type" content{{=}}"text/html; charset{{=}}utf-8"&gt;
&lt;title&gt;validity.typeMismatch&lt;/title&gt;
&lt;/head&gt;

&lt;body&gt;
&lt;form name{{=}}"frmRegister" id{{=}}"frmRegister"&gt;
&lt;label&gt;Email Address:&lt;br&gt;&lt;input name{{=}}"txtemail" id{{=}}"txtemail" required{{=}}"required" type{{=}}"email"&gt;&lt;/label&gt;
&lt;input type{{=}}"submit" value{{=}}"Register.."&gt;
&lt;/form&gt;
&lt;script type{{=}}"text/javascript"&gt;
function validEmail(evt){
var el{{=}}evt.target;
if(el.validity){
// html5 aware browsers
if(el.validity.typeMismatch){
el.setCustomValidity('Please enter a valid email address.');
}else{
el.setCustomValidity("");
}
}else{
// legacy validation

}
}
document.getElementById('txtemail').addEventListener('blur',validEmail,false);
&lt;/script&gt;


&lt;/body&gt;&lt;/html&gt;
}}
}}
{{Notes_Section
|Usage=Use to validate input fields of type email or url instead of patternMismatch.
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
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN, HTML5Rocks
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh773366(v=vs.85).aspx typeMismatch Property]
|HTML5Rocks_link=[http://www.html5rocks.com/en/tutorials/forms/html5forms/ Making forms fabulous]
}}