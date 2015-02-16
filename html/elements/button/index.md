{{Page_Title|button}}
{{Flags
|State=In Progress
|Editorial notes=Add Category, Parent, Children and Compatibility information.
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The '''button''' element represents a clickable button.|The "button" tag is one of many ways to create buttons on an HTML page_ A web developer can also use the "input" tag in conjunction with type="button" or by styling an "a" tag to achieve the same functionality. However, those may be harder and their results may not be as clean.
}}
{{Markup_Element
|DOM_interface=dom/HTMLButtonElement
|Content=You can put text or images inside a button element. If the element is not disabled, the user can activate the button.

By default, the button element is used to submit [[html/elements/form|'''form''']] data. Modifying the type attribute can change this behavior.

===Attributes (HTML 4)===
<dl>
<dt>name</dt>
<dd>The name of the button. This can be used to identify which button was used to submit a form.</dd>
<dt>type</dt>
<dd>This specifies the type of the button. If omitted, the type is <code>submit</code>. The following types are possible:
<ul>
<li><code>submit</code>:  the button submits the form it is associated with and sends the form data to the server. This is the default value.</li>
<li><code>reset</code>: the button resets the form it is associated with. This will set the containing fields to their initial values.</li>
<li><code>button</code>: the button has no default behavior.  Useful to bind JavaScript [[dom/MouseEvent/click|'''click''']] events</li> 
</ul>
</dd>
<dt>value</dt>
<dd>The initial value of the button.</dd>
<dt>disabled</dt>
<dd>This Boolean attribute indicates that the user cannot interact with the button. If this attribute is not specified, the button inherits its setting from the containing element, for example '''fieldset''' if there is no containing element with the disabled attribute set, then the button is enabled. A disabled button isn’t clickable.</dd>
</dl>

===Additional attributes (HTML 5, candidate specification)===
<dl>
<dt>autofocus</dt>
<dd>When this attribute is set to "true" the button will have input focused after the page loads, unless the user overrides it, for example by typing in a different control. Only one form-associated element in a document can have this attribute specified.</dd>
<dt>form</dt>
<dd>Specifies which form the button is associated with. The value of the attribute must be the id attribute of the form. If this attribute is not specified, the button must be a descendant of the form itself to be able to submit form data. This attribute enables you to place '''button''' elements anywhere within a document, not just as descendants of their '''form''' elements.</dd>
<dt>formaction</dt>
<dd>The URI of a program that processes the information from the form. When present, it will override the action attribute of the associated form.</dd>
<dt>formmethod</dt>
<dd>The HTTP method to send the form data. This can either be <code>post</code> or <code>get</code>. If specified, it will override the method attribute of the associated form.
Possible values are:
* <code>post</code>: The data from the form is included in the body of the form and is sent to the server.
* <code>get</code>: The data from the form are appended to the form attribute URI, with a '?' as a separator, and the resulting URI is sent to the server. Use this method when the form has no side-effects and contains only ASCII characters.</dd>
<dt>formnovalidate</dt>
<dd>If the button is a submit button, this attribute specifies whether the form should be validated or not. It overrides the '''novalidate''' attribute of the form it belongs to.</dd>
<dt>formtarget</dt>
<dd>This attribute is a keyword, indicating where to display the response that is received after submitting the form. This can be one of the following:
<ul>
<li><code>_self</code>: load the response into the same context as the form itself. This is the default value.</li>
<li><code>_blank</code>: load the response into a new, unnamed context (Browser window)</li>
<li><code>_parent</code>: loads the response into the parent context. If there is no parent, it will behave the same as _self.</li>
<li><code>_top</code>: loads the response into the top-most context. This is the browsing context of an ancestor of the current context. If there is no parent, it will behave the same as _self.</li>
</ul>
</dd>
</dl>

All these attributes, except <code>name</code>, have default values and can be omitted.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This examples uses the <code>&lt;button&gt;</code> element to display a clickable button with out sending or reseting a form.
|Code=<button name="myButton" type="button">Click me</button>
|LiveURL=http://code.webplatform.org/gist/b08191a8d5915621a5e1
}}{{Single Example
|Language=HTML
|Description=This example shows how to use a submit <code>&lt;button&gt;</code> to send a form. Read about the [[html/elements/form|'''form''']] element to get further information about how to use forms.
|Code=<form action="dataReceiverURI">
  <label for="name">Name:</label>
  <input id="name" type="text" name="user_name">
  <button name="mySubmitButton">Submit</button>
</form>
|LiveURL=http://code.webplatform.org/gist/ceb6531b1b86fb0b21d0
}}{{Single Example
|Language=HTML
|Description=This example shows how to reset a form with use of <code>&lt;button=&quot;reset&quot;&gt;</code>. Read about the [[html/elements/form|'''form''']] element to get further information about how to use forms.
|Code=<form>
  <label for="name">Name:</label>
  <input id="name" type="text" name="user_name" >
  <button name="myResetButton">reset</button>
</form>
|LiveURL=http://code.webplatform.org/gist/c579515bcd4378bfd634
}}
}}
{{Notes_Section
|Usage=Generally, the '''button''' element can be used whenever there should be a button clickable by the user. 

The ending tag is mandatory. The button should have a descriptive text inside it, otherwise the button will be empty and the user won't know what the button will do.

Please note that styling a submit button using the &lt;button&gt; element is easier than styling an [[html/elements/input|'''input''']] element with type <code>submit</code>.
|Notes=Since the default for the <code>type</code> attribute is <code>submit</code>, the type can be omitted if no other type needs to be used. Historical browser versions may have different standard <code>type</code> values.

Firefox for Android, by default, sets a <code>[[css/properties/background-image|background-image]]</code> gradient on all '''button''' elements. This can be disabled using <code>background-image: none</code>.

Firefox will, unlike other browsers, by default, [http://stackoverflow.com/questions/5985839/bug-with-firefox-disabled-attribute-of-input-not-resetting-when-refreshing persist the dynamic disabled state] of a '''button''' across page loads. Setting the value of the <code>autocomplete</code> attribute to <code>off</code> disables this feature. See [https://bugzilla.mozilla.org/show_bug.cgi?id=654072 Mozilla Bug #654072].

===Clicking and focus===
Whether clicking on a '''button''' causes it to (by default) become focused varies by browser and OS.

Does clicking on a '''button''' give it the focus?:
{{{!}} class="wikitable"
! Desktop Browsers
! Windows 8.1
! OS X 10.9
{{!}}-
{{!}} Firefox 30.0
{{!}} Yes
{{!}} No (even with a [[html/attributes/tabIndex|<code>tabindex</code>]])
{{!}}-
{{!}} Chrome 35
{{!}} Yes
{{!}} Yes
{{!}}-
{{!}} Safari 7.0.5
{{!}} N/A
{{!}} No (even with a [[html/attributes/tabIndex|<code>tabindex</code>]])
{{!}}-
{{!}} Internet Explorer 11
{{!}} Yes
{{!}} N/A
{{!}}-
{{!}} Presto (Opera 12)
{{!}} Yes
{{!}} ???
{{!}}}


Does tapping on a '''button''' give it the focus?:
{{{!}} class="wikitable"
! Mobile Browsers
! iOS 7.1.2
! Android 4.4.4
{{!}}-
{{!}} Safari Mobile
{{!}} No (even with a [[html/attributes/tabIndex|<code>tabindex</code>]])
{{!}} N/A
{{!}}-
{{!}} Chrome 35
{{!}} ???
{{!}} Yes
{{!}}}
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related_Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/forms.html#the-button-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related_Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/forms.html#the-button-element
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related_Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/interact/forms.html#edef-BUTTON
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Topic_clusters=Document Structure, HTML
|Manual_links=* [[html/elements/input/type/button|'''input type="button"''']]
* [[html/elements/input/type/submit|'''input type="submit"''']]
|External_links=
|Manual_sections=
}}
{{Topics|HTML, UI}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/button <button> on MDN]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
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
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=8 and later
|Note=The default value of the type attribute depends on the current document compatibility mode. In IE8 Standards mode, the default value is submit. In other compatibility modes and earlier versions of Windows Internet Explorer, the default value is button. When the BUTTON element is submitted in a form, the value depends on the current document compatibility mode. In IE8 mode, the value attribute is submitted. In other document modes and earlier versions of Internet Explorer, the innerText value is submitted.
}}
}}