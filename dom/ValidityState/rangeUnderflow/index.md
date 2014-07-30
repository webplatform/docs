{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Returns whether a value is less than the '''min''' attribute on an input control.}}
{{API_Object_Property
|Property_applies_to=dom/ValidityState
|Read_only=Yes
|Example_object_name=element.validity
|Return_value_name=rangeUnderflow
|Javascript_data_type=Boolean
|Return_value_description=Whether a value is less than the '''min''' attribute.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example validates a numeric (type="number") input field on the onblur event handler. If a number outside the range values of the input control is entered the custom validity message is displayed when the form is submitted.
|Code=&lt;label&gt;Enter a number between 4 and 20&lt;br/&gt;
&lt;input id{{=}}"myField" type{{=}}"number" required  min{{=}}"4" max{{=}}"20" step{{=}}"2" /&gt;&lt;/label&gt;
&lt;script type{{=}}"text/javascript"&gt;
var el{{=}}document.getElementById('myField');
function validRange(evt){
var el=evt.target;
if(el.validity){
// HTML5 aware browsers
if(el.validity.rangeOverflow||el.validity.rangeUnderflow){
el.setCustomValidity('The entered number is outside the acceptable range.')
}else{
el.setCustomValidity("");
}
}else{
// legacy validation

}
}
el.addEventListener('blur',validRange,false);
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
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN, HTML5Rocks
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh773360(v=vs.85).aspx rangeUnderflow Property]
|HTML5Rocks_link=[http://www.html5rocks.com/en/tutorials/forms/html5forms/ Making forms fabulous]
}}