{{Page_Title}}
{{Flags
|Content=Broken Links, Compatibility Incomplete
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The '''input''' element (&lt;input&gt;) is a multipurpose element for representing form widgets. The type of widget depends on the <code>type</code> attribute.}}
{{Markup_Element
|DOM_interface=dom/HTMLInputElement
|Content====HTML information===
{{{!}} class="wikitable"
{{!}}-
!Closing Tag
{{!}}The input element is a void element. An input element must have a start tag but must not have an end tag
{{!}}-
!CSS Display
{{!}}inline
{{!}}-
!HTML Element Categories
{{!}}flow phrasing interactive
{{!}}}

The input element behavior varies depending on the value of its [[html/elements/input/type|type]] attribute:
* [[html/elements/input/type/button|type=button]]
* [[html/elements/input/type/checkbox|type=checkbox]]
* [[html/elements/input/type/color|type=color]]
* [[html/elements/input/type/date|type=date]]
* [[html/elements/input/type/datetime-local|type=datetime-local]]
* [[html/elements/input/type/email|type=email]]
* [[html/elements/input/type/file|type=file]]
* [[html/elements/input/type/hidden|type=hidden]]
* [[html/elements/input/type/image|type=image]]
* [[html/elements/input/type/month|type=month]]
* [[html/elements/input/type/number|type=number]]
* [[html/elements/input/type/password|type=password]]
* [[html/elements/input/type/radio|type=radio]]
* [[html/elements/input/type/range|type=range]]
* [[html/elements/input/type/reset|type=reset]]
* [[html/elements/input/type/time|type=time]]
* [[html/elements/input/type/search|type=search]]
* [[html/elements/input/type/submit|type=submit]]
* [[html/elements/input/type/tel|type=tel]]
* '''[[html/elements/input/type/text|type=text]]''' (default if type is not set or empty)
* [[html/elements/input/type/url|type=url]]
* [[html/elements/input/type/week|type=week]]

Other valid attributes for the input element are <code>[[html/elements/input/accept|accept]]</code>, <code>[[html/elements/input/alt|alt]]</code>, <code>[[html/elements/input/autocomplete|autocomplete]]</code>, <code>[[html/elements/input/autofocus|autofocus]]</code>, <code>[[html/elements/input/checked|checked]]</code>, <code>[[html/elements/input/dirname|dirname]]</code>, <code>[[html/elements/input/disabled|disabled]]</code>, <code>[[html/elements/input/form|form]]</code>, <code>[[html/elements/input/formaction|formaction]]</code>, <code>[[html/elements/input/formenctype|formenctype]]</code>, <code>[[html/elements/input/formmethod|fommethod]]</code>, <code>[[html/elements/input/formnovalidate|formnovalidate]]</code>, <code>[[html/elements/input/formtarget|formtarget]]</code>, <code>[[html/elements/input/height|height]]</code>, <code>[[html/elements/input/list|list]]</code>, <code>[[html/elements/input/max|max]]</code>, <code>[[html/elements/input/maxlength|maxlength]]</code>, <code>[[html/elements/input/min|min]]</code>, <code>[[html/elements/input/multiple|multiple]]</code>, <code>[[html/elements/input/name|name]]</code>, <code>[[html/elements/input/pattern|pattern]]</code>, <code>[[html/elements/input/placeholder|placeholder]]</code>, <code>[[html/elements/input/readonly|readonly]]</code>, <code>[[html/elements/input/required|required]]</code>, <code>[[html/elements/input/size|size]]</code>, <code>[[html/elements/input/src|src]]</code>, <code>[[html/elements/input/step|step]]</code>, <code>[[html/elements/input/value|value]]</code>, <code>[[html/elements/input/width|width]]</code>, and global element attributes. Note that some attributes do not apply for certain types.

Internationalization topics related to the <code>input</code> element:
* [http://www.w3.org/International/techniques/authoring-html#formdir Managing text direction in form controls]
* [http://www.w3.org/International/techniques/authoring-html#localdata Working with date formats]
* [http://www.w3.org/International/techniques/authoring-html#localnames Working with personal names]
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''input''' element to create different types of input controls.
|Code=<form action="http://example.org/survey" method=post>
<p>Name</p>
<br><input name="control1" type="text" value="Your Name">
<P>Password</P>
<br><input type="password" name="control2">
<p>Color</p>
<br><input type="radio" name="control3" value="0" checked>Red
<input type="radio" name="control3" value="1">Green
<input type="radio" name="control3" value="2">Blue
<p>Comments</p>
<br><input type="TEXT" name="control4" size="20,5" maxlength="250">
<p><input name="control5" type=checkbox checked>Send receipt</p>
<p><input type="submit" value="OK"><input type="reset" value="reset"></p>
</form>
|LiveURL=http://code.webplatform.org/gist/6364130
}}
}}
{{Notes_Section
|Usage=To cater for international users see: [http://www.w3.org/International/techniques/authoring-html#form-dir Managing text direction in form controls]
|Notes=For code samples, see [http://go.microsoft.com/fwlink/p/?LinkID{{=}}251128 Form controls part 1] and [http://go.microsoft.com/fwlink/p/?LinkID{{=}}251131 Form controls part 2: validation] on the Windows Internet Explorer sample site.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML5
|URL=http://www.w3.org/TR/html5/forms.html#the-input-element
|Status=W3C Candidate Recommendation
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
|Topic_clusters=HTML
|External_links=http://www.w3.org/TR/html-markup/input.html#input
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}