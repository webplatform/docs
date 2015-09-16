---
title: toJSON
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/cc907896(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Used by the JSON.stringify method to enable the transformation of an object''s data for JavaScript Object Notation (JSON) serialization.'
tags:
  - JS
  - Basic
uri: javascript/Date/toJSON

---
## Summary

Used by the JSON.stringify method to enable the transformation of an object's data for JavaScript Object Notation (JSON) serialization.

## Syntax

<span class="language">JavaScript</span>

    objectname.toJSON()

**objectname**
:   Required. An object for which JSON serialization is wanted.

## Examples

The following example uses the toJSON method to serialize string member values in uppercase. The toJSON method is called when JSON.stringify is called.

``` js
var contact = new Object();
 contact.firstname = "Jesper";
 contact.surname = "Aaberg";
 contact.phone = ["555-0100", "555-0120"];

 contact.toJSON = function(key)
  {
     var replacement = new Object();
     for (var val in this)
     {
         if (typeof (this[val]) === 'string')
             replacement[val] = this[val].toUpperCase();
         else
             replacement[val] = this[val]
     }
     return replacement;
 };

 var jsonText = JSON.stringify(contact);

 /* The value of jsonText is:
 '{"firstname":"JESPER","surname":"AABERG","phone":["555-0100","555-0120"]}'
 */
```

The following example illustrates how to use the toJSON method that is a built-in member of the [Date](/javascript/Date) object.

``` js
var dt = new Date('8/24/2009');
 dt.setUTCHours(7, 30, 0);
 var jsonText = JSON.stringify(dt);

 /* The value of jsonText is:
 '"2009-08-24T07:30:00Z"'
 */
```

## Remarks

The toJSON method is used by the JSON.stringify function.JSON.stringify serializes a JavaScript value into JSON text. If a toJSON method is provided to JSON.stringify , the toJSON method is called when JSON.stringify is called.

The toJSON method is a built-in member of the [Date](/javascript/Date) JavaScript object. It returns an ISO-formatted date string for the UTC time zone (denoted by the suffix Z).

You can override the toJSON method for the Date type, or define a toJSON method for other object types to achieve transformation of data for the specific object type before JSON serialization.

## See also

### Other articles

-   [JSON Object](/javascript/JSON)
-   [JSON.parse Function](/javascript/JSON/parse)
-   [JSON.stringify Function](/javascript/JSON/stringify)
-   [JavaScript Methods](/javascript/methods)

