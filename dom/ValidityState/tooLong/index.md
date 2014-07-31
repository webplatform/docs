{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Returns whether an input field's value is longer than is allowed by the '''maxlength''' attribute.}}
{{API_Object_Property
|Property_applies_to=dom/ValidityState
|Read_only=Yes
|Example_object_name=element.validity
|Return_value_name=result
|Javascript_data_type=Boolean
|Return_value_description=Whether a value is longer than is allowed by the '''maxlength''' attribute.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=In the following example the tooLong property is used to validate the length of text entered into a text area. However, the validity.tooLong is always false since text greater than the maxlength attribute value cannot be entered.
|Code=&lt;!DOCTYPE html&gt;
&lt;html&gt;&lt;head&gt;
&lt;meta http-equiv{{=}}"Content-Type" content{{=}}"text/html; charset{{=}}utf-8"&gt;
&lt;title&gt;validity.tooLong&lt;/title&gt;
&lt;/head&gt;

&lt;body&gt;
&lt;form name{{=}}"frmtwit" id{{=}}"frmtwit"&gt;
&lt;label&gt;Message:&lt;br&gt;&lt;textarea id{{=}}"txtMessage" maxlength{{=}}"12"&gt;&lt;/textarea&gt;&lt;/label&gt;
&lt;input type{{=}}"submit" value{{=}}"Twit.."&gt;
&lt;/form&gt;
&lt;script type{{=}}"text/javascript"&gt;
function validLength(evt){
var el{{=}}evt.target;
if(el.validity){
// html5 aware browsers
if(el.validity.tooLong){
el.setCustomValidity('Your twit is too long to be sent.');
}else{
el.setCustomValidity("");
}
}else{
// legacy validation

}
}
document.getElementById('txtMessage').addEventListener('blur',validLength,false);
&lt;/script&gt;


&lt;/body&gt;&lt;/html&gt;
}}
}}
{{Notes_Section
|Usage=There seems to be little usage for the tooLong validity state test as textarea and input elements do not allow text input past the maxlength value.


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
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh773365(v=vs.85).aspx tooLong Property]
|HTML5Rocks_link=[http://www.html5rocks.com/en/tutorials/forms/html5forms/ Making forms fabulous]
}}