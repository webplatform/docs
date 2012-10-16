{{Page_Title}}
{{Flags
|High-level issues=Needs Topics
|Content=Incomplete,  Compatibility Incomplete,
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section}}
{{Markup_Element
|DOM_interface=dom/HTMLInputElement
|Content====HTML information===
{{{!}} class="wikitable"
{{!}}-
!Closing Tag
{{!}}required
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
* [[html/elements/input/type/email|type=email]]
* [[html/elements/input/type/file|type=file]]
* [[html/elements/input/type/hidden|type=hidden]]
* [[html/elements/input/type/image|type=image]]
* [[html/elements/input/type/number|type=number]]
* [[html/elements/input/type/password|type=password]]
* [[html/elements/input/type/radio|type=radio]]
* [[html/elements/input/type/range|type=range]]
* [[html/elements/input/type/reset|type=reset]]
* [[html/elements/input/type/search|type=search]]
* [[html/elements/input/type/submit|type=submit]]
* [[html/elements/input/type/tel|type=tel]]
* '''[[html/elements/input/type/text|type=text]]''' (default if type is not set or empty)
* [[html/elements/input/type/url|type=url]]

}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''input''' element to create different types of input controls.
|Code=&lt;form action{{=}}"http://example.org/survey" method{{=}}post&gt;
&lt;p&gt;Name&lt;/p&gt;
&lt;br&gt;&lt;input name{{=}}"control1" type{{=}}text value{{=}}"Your Name"&gt;
&lt;P&gt;Password&lt;/P&gt;
&lt;br&gt;&lt;input type{{=}}"password" name{{=}}"control2"&gt;
&lt;p&gt;Color&lt;/p&gt;
&lt;br&gt;&lt;input type{{=}}"radio" name{{=}}"control3" value{{=}}"0" checked&gt;Red
&lt;input type{{=}}"radio" name{{=}}"control3" value{{=}}"1"&gt;Green
&lt;input type{{=}}"radio" name{{=}}"control3" value{{=}}"2"&gt;Blue
&lt;p&gt;Comments&lt;/p&gt;
&lt;br&gt;&lt;input type{{=}}"TEXT" name{{=}}"control4" size{{=}}"20,5" maxlength{{=}}"250"&gt;
&lt;p&gt;&lt;input name{{=}}"control5" type{{=}}checkbox checked&gt;Send receipt&lt;/p&gt;
&lt;p&gt;&lt;input type{{=}}"submit" value{{=}}"OK"&gt;&lt;input type{{=}}"reset" value{{=}}"reset"&gt;&lt;/p&gt;
&lt;/form&gt;
}}
}}
{{Notes_Section
|Notes=For code samples, see [http://go.microsoft.com/fwlink/p/?LinkID{{=}}251128 Form controls part 1] and [http://go.microsoft.com/fwlink/p/?LinkID{{=}}251131 Form controls part 2: validation] on the Windows Internet Explorer sample site.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML5
|URL=http://www.w3.org/TR/html5/the-input-element.html#the-input-element
|Status=W3C Working Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}