{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Sets the URL which the browser will send the form data on submission.}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement/form
|Content=The action attribute is applied to a form element in order to instruct the browser of where to send the data upon submission. If it is not specified, the browser will automatically send data back to the current address.

=== Best practices ===
It is recommended that you use an absolute URL for the action instead of a relative URL. Using an absolute URL means you know exactly where the form is going all the time, a relative URL may cause it to go to other places if you are not careful.

===Mailto actions===
It is possible to make an email form by placing an mailto address in the action attribute. Although it is technically possible, we recommend strongly to 'not' use them, as it doesn't work in every browser as it was once supposed to. Please use an email script instead, and make the form post to that certain email script.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''action''' attribute to post a form to a specified URL.
|Code=<!doctype html>
<title>Contact Form Demonstration</title>

<!-- We are instructing the browser that this form will be submitted to the URL in the action attribute. -->
<form action="http://example.com/contact" method="post">
    <label for="email">Email: </label>
    <input id="email" name="email" type="email" required>

    <label for="name">Name:</label>
    <input id="name" name="name" required>

    <label for="message">Message: </label>
    <textarea id="message" name="message">
    </textarea>

    <button>Submit</button>
</form>
}}
}}
{{Notes_Section
|Notes====Remarks===
Windows Internet Explorer 8 or later. In IE8 Standards mode, the value of the '''action''' attribute depends on the context of the reference to the attribute.  When read as a Document Object Model (DOM) attribute,  '''action''' returns an absolute URL.  The value specified by the page author is returned when '''action''' is read as a content attribute, when the page is displayed in an earlier document compatibility mode, or when the page is viewed with an earlier version of the browser.  For more information, see Attribute Differences in Internet Explorer 8.
The value of the '''action''' attribute depends on the context of the reference to the attribute.  When read as a DOM attribute,  '''action''' returns an absolute URL.  The value specified by the page author is returned when '''action''' is read as a content attribute.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML5
|URL=http://www.w3.org/TR/html5/forms.html#attr-fs-action
|Status=Candidate Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=Beta
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=3
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=3
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=0.8
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=1
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=6
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=Beta
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=14
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=2
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=3
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_version=Beta
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=3
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=HTML
|Manual_sections====Related pages===
* [[html/elements/form|HTML Form Element]]
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}