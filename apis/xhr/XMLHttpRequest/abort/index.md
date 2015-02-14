{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Stops an asynchronous XMLHttpRequest in progress.}}
{{API_Object_Method
|Parameters=
|Method_applies_to=apis/xhr/XMLHttpRequest
|Example_object_name=
|Return_value_name=
|Javascript_data_type=void
|Return_value_description=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=function request() {
    var xhr = new XMLHttpRequest();
    xhr.open("GET", "http://localhost/test.xml", true);
    xhr.onreadystatechange = handler;
    xhr.send();
    return xhr;
}

document.getElementById('submit').addEventListener('click', function () {
    var xhr = request(),
        submit = this,
        cancel = document.getElementById('cancel');
    
    function detach() {
        submit.removeEventListener('click', canceling, false);
        cancel.removeEventListener('click', canceling, false);
    }
    
    function canceling() {
        detach();
        xhr.abort();
    }
    
    // detach any remaining handlers after XHR finishes
    xhr.addEventListener('load', detach, false);
    
    // cancel if "Submit" is clicked again before XHR finishes
    submit.addEventListener('click', canceling, false);
    
    // cancel if "Cancel" is clicked
    cancel.addEventListener('click', canceling, false);
}, false);
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=Calling '''abort''' resets the object; the '''readyState''' is changed to 0 (uninitialized).
Calling it on an already aborted request throws an exception.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C XMLHttpRequest Specification
|URL=http://www.w3.org/TR/XMLHttpRequest/
|Status=W3C Working Draft
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|API, XHR}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=23.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=16.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.1
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=3.0
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=7.0
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=5.0
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}