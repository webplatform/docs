{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Returns whether the input field value does not match the rules defined by the pattern attribute.}}
{{API_Object_Property
|Property_applies_to=dom/ValidityState
|Read_only=Yes
|Example_object_name=element.validity
|Return_value_name=result
|Javascript_data_type=Boolean
|Return_value_description=Whether a value does not match the rules defined by the '''pattern''' attribute.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example validates a UK Postal code field on the blur event handler. If an invalid UK postal code is entered, when the form is submitted the custom validity message is displayed.
|Code=&lt;script type{{=}}"text/javascript"&gt;
function validatePostCode(evt){
var el{{=}}evt.target;
if(el.validity){
// HTML5 aware browsers
if(el.validity.patternMismatch){
el.setCustomValidity('Not a valid UK Postal Code.eg:G1 1AA ');
}else{
el.setCustomValidity("");
}
}else{
// fallback for legacy browsers.


}
}
document.getElementById('txtPostcode').addEventListener('blur',validatePostCode,false);
&lt;/script&gt;
}}
}}
{{Notes_Section}}
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
{{See_Also_Section
|Manual_links=[http://www.regexlib.com/ Regular Expression Library]
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN, HTML5Rocks
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh773355(v=vs.85).aspx patternMismatch Property]
|HTML5Rocks_link=[http://www.html5rocks.com/en/tutorials/forms/html5forms/ Making forms fabulous]
}}