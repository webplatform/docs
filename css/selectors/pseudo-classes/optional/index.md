---
title: ':optional'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: ':optional'
  topic: css
notes:
  - 'Needs title, summary, spec reference, standardization status, fix table coding, remove topic cluster flags'
readiness: 'Not Ready'
tags:
  - CSS_Selectors
  - CSS
  - Needs_Summary
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - selection
uri: 'css/selectors/pseudo-classes/:optional'

---
=

<dl>
<dd>
optional=

</dd>
</dl>

## Examples

The following example puts a green border on a field when it is valid and a red border with bold text when it isn't. The email field is required, but the others aren't. The URL field is pre-filled with a bad URL, so it isn't valid when the page opens. In addition, the two optional fields are styled with light gray backgrounds, and the required field with an eye-catching yellow background.

``` html
<!DOCTYPE html >
<html>
<head>
  <title>:valid/:invalid Pseudo-class Example</title>
  <style type="text/css">

  #PC1 input:valid {
    border:solid lime;
    font-weight:normal;
  }
  #PC1 input:invalid {
    border:solid red;
    font-weight:bold;
  }
  #PC1 input:required {
    background-color:Yellow;
  }
  #PC1 input:optional {
    background-color:LightGray;
  }
  </style>
</head>
<body>
  <form id="PC1">
    <p><label>Enter some text: <input type="text"/></label></p>
    <p><label>*Enter a valid email address: <input type="email" required /></label></p>
    <p><label>Enter a valid URL: <input type="url" value="not a url"/></label></p>
    <p>* required field</p>
  </form>
</body>
</html>
```

## Notes

### Remarks

An *optional* field is defined as any [input](http://go.microsoft.com/fwlink/p/?LinkID=219805) field that can accept the [required](http://go.microsoft.com/fwlink/p/?LinkId=233321) attribute but does not have it set, plus any [select](http://go.microsoft.com/fwlink/p/?LinkId=233312) and [textarea](http://go.microsoft.com/fwlink/p/?LinkID=236896) elements that don't have the [required](http://go.microsoft.com/fwlink/p/?LinkId=233321) attribute set.

### Syntax

selector

<dl>
<dd>
optional

</dd>
</dl>
### Parameters

*selector*
:   A CSS simple selector.

## See also

### Related articles

#### Pseudo-Classes

-   [:target pseudo-class selector](/CSS/Selectors/pseudo-classes/:target)

-   [:-ms-input-placeholder](/css/selectors/pseudo-classes/:-ms-input-placeholder)

-   [:checked](/css/selectors/pseudo-classes/:checked)

-   [:disabled](/css/selectors/pseudo-classes/:disabled)

-   [:empty](/css/selectors/pseudo-classes/:empty)

-   [:enabled](/css/selectors/pseudo-classes/:enabled)

-   [:first-child](/css/selectors/pseudo-classes/:first-child)

-   [:first-of-type](/css/selectors/pseudo-classes/:first-of-type)

-   [:focus](/css/selectors/pseudo-classes/:focus)

-   [:in-range](/css/selectors/pseudo-classes/:in-range)

-   [:indeterminate](/css/selectors/pseudo-classes/:indeterminate)

-   [:invalid](/css/selectors/pseudo-classes/:invalid)

-   [:lang(c)](/css/selectors/pseudo-classes/:lang(c))

-   [:last-of-type](/css/selectors/pseudo-classes/:last-of-type)

-   [:nth-child(n)](/css/selectors/pseudo-classes/:nth-child(n))

-   [:nth-last-child(n)](/css/selectors/pseudo-classes/:nth-last-child(n))

-   [:nth-last-of-type(n)](/css/selectors/pseudo-classes/:nth-last-of-type(n))

-   [:nth-of-type(n)](/css/selectors/pseudo-classes/:nth-of-type(n))

-   [:only-child](/css/selectors/pseudo-classes/:only-child)

-   [:only-of-type](/css/selectors/pseudo-classes/:only-of-type)

-   **:optional**

-   [:required](/css/selectors/pseudo-classes/:required)

-   [:root](/css/selectors/pseudo-classes/:root)

-   [:target](/css/selectors/pseudo-classes/:target)

-   [:valid](/css/selectors/pseudo-classes/:valid)

#### Selectors

-   [querySelectorAll](/css/selectors_api/querySelectorAll)

-   [ID](/css/selectors/ID)

-   [Namespaced](/css/selectors/Namespaced)

-   [Universal](/css/selectors/Universal)

-   [equality](/css/selectors/attributes/equality)

-   [Attribute selector](/css/selectors/attributes/existence)

-   [hyphen](/css/selectors/attributes/hyphen)

-   [prefix](/css/selectors/attributes/prefix)

-   [substring](/css/selectors/attributes/substring)

-   [suffix](/css/selectors/attributes/suffix)

-   [whitespace](/css/selectors/attributes/whitespace)

-   [:-ms-input-placeholder](/css/selectors/pseudo-classes/:-ms-input-placeholder)

-   [:checked](/css/selectors/pseudo-classes/:checked)

-   [:disabled](/css/selectors/pseudo-classes/:disabled)

-   [:empty](/css/selectors/pseudo-classes/:empty)

-   [:enabled](/css/selectors/pseudo-classes/:enabled)

-   [:first-child](/css/selectors/pseudo-classes/:first-child)

-   [:first-of-type](/css/selectors/pseudo-classes/:first-of-type)

-   [:focus](/css/selectors/pseudo-classes/:focus)

-   [:in-range](/css/selectors/pseudo-classes/:in-range)

-   [:indeterminate](/css/selectors/pseudo-classes/:indeterminate)

-   [:invalid](/css/selectors/pseudo-classes/:invalid)

-   [:lang(c)](/css/selectors/pseudo-classes/:lang(c))

-   [:last-of-type](/css/selectors/pseudo-classes/:last-of-type)

-   [:nth-child(n)](/css/selectors/pseudo-classes/:nth-child(n))

-   [:nth-last-child(n)](/css/selectors/pseudo-classes/:nth-last-child(n))

-   [:nth-last-of-type(n)](/css/selectors/pseudo-classes/:nth-last-of-type(n))

-   [:nth-of-type(n)](/css/selectors/pseudo-classes/:nth-of-type(n))

-   [:only-child](/css/selectors/pseudo-classes/:only-child)

-   [:only-of-type](/css/selectors/pseudo-classes/:only-of-type)

-   **:optional**

-   [:required](/css/selectors/pseudo-classes/:required)

-   [:root](/css/selectors/pseudo-classes/:root)

-   [:target](/css/selectors/pseudo-classes/:target)

-   [:valid](/css/selectors/pseudo-classes/:valid)

-   [::selection](/w/index.php?title=selection&action=edit&redlink=1)

-   [type](/css/selectors/type)

### Related pages

-   HTML5 Forms (Internet Explorer 10 Guide for Developers)[HTML5 Forms (Internet Explorer 10 Guide for Developers)](http://go.microsoft.com/fwlink/p/?LinkId=238198)
-   required attribute[required attribute](http://go.microsoft.com/fwlink/p/?LinkId=233321)
-   `Related pseudo-classes`
-   :invalid[:invalid](/css/selectors/pseudo-classes/:invalid)
-   :required[:required](/css/selectors/pseudo-classes/:required)
-   :valid[:valid](/css/selectors/pseudo-classes/:valid)
