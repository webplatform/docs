---
title: JSON
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: "JSON is a native API for parsing and serialising information to the JSON format.\n"
tags:
  - API
  - Objects
  - JavaScript
uri: apis/json

---
## <span>Summary</span>

JSON is a native API for parsing and serialising information to the JSON format.

JSON contains two methods: `parse` for parsing JSON strings, and `stringify` for converting a JavaScript object into JSON.

## <span>Properties</span>

*No properties.*

## <span>Methods</span>

API Name
:   Summary

[parse](/apis/json/parse)
:   Parse a JSON string to a JavaScript object.

[stringify](/apis/json/stringify)
:   Export a JavaScript object to a JSON string.

## <span>Events</span>

*No events.*

## <span>Examples</span>

Convert a JavaScript object to a string.

``` js
var js_object = {
    type: "This is a Javascript Object."
};

var json_string = JSON.stringify(js_object);
```

Parse a JSON string to a JavaScript object.

``` js
var json_string = '{type:"This is a JSON Object."}';
var js_object = JSON.parse(json_string);
alert(js_object.type);
```

## <span>Notes</span>

Browsers without JSON support can be polyfilled using third party JavaScript libraries.

## <span>Related specifications</span>

[JSON-LD 1.0](http://www.w3.org/TR/json-ld/)
:   W3C Recommendation
