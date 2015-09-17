---
title: 'cookie'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Document
    href: /dom/Document
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/Document
standardization_status: 'W3C Recommendation'
summary: 'Sets or gets the string value of a cookie.'
tags:
  - API_Object_Properties
  - DOM
uri: dom/Document/cookie

---
## Summary

Sets or gets the string value of a cookie.

Property of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## Syntax

``` js
var cookies = document.cookie;
document.cookie = newCookie;
```

## Return Value

Returns an object of type StringString

The current cookies of the document.

## Examples

``` js
//set a cookie with a name, a value, and a number of days before expiring
function setCookie(aname, avalue, expdays) {
    var dt = new Date();
    dt.setTime(dt.getTime() + (expdays*24*60*60*1000));
    var expires = "expires=" + dt.toGMTString();
    document.cookie = aname + "=" + avalue + "; " + expires;
}

//retrieve all document cookies; if passed cookie name found, return value
//if passed cookie name not found, return null
function getCookie(aname) {
    var name = aname + "=";
    var carray = document.cookie.split(';');
    for(var i = 0; i < carray.length; i++) {
        var cn = carray[i];
        if (cn.indexOf(name) == 0) return cn.substring(name.length,cn.length);
    }
    return "";
}
```

## Usage

     A cookie is a small piece of information. Each cookie is stored in a name=value pair called a crumb—that is, if the cookie name is "id" and you want to save the id value as "this," the cookie is saved as id=this. You can store up to a maxium of 50 name=value pairs in a cookie; the cookie is always returned as a string of all the cookies that apply to the document. This means that you must parse the string returned to find the values of individual cookies.

Cookies accumulate each time the property is set. Once the maximum pair limit is reached, subsequent set will push older name=value pair off in favor of the new name=value pair. You can use the [split](/concepts/programming/javascript/core_objects#String_Object) method to extract a value stored in a cookie.

## Related specifications

[DOM Level 2 HTML](http://www.w3.org/TR/DOM-Level-2-HTML/)
:   Recommendation

[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage)
:   Living Standard

[W3C HTML5](http://www.w3.org/TR/html5/)
:   Working Draft
