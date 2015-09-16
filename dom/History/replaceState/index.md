---
title: replaceState
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'General clean-up'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/History
    href: /dom/History
standardization_status: 'W3C Working Draft'
summary: 'Overwrites the current history record with a new record.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/History/replaceState

---
## Summary

Overwrites the current history record with a new record.

Method of [dom/History](/dom/History)[dom/History](/dom/History)

## Syntax

``` js
 history.replaceState(statedata, title, url);
```

## Parameters

### statedata

 Data-type
:   any

 The data to update.

### title

 Data-type
:   String

 The data title to update.

### url

 Data-type
:   String

(Optional)

The data URL to update.

## Return Value

No return value

## Examples

In the following example, a user stored a preference where they want to go straight to the User Account page when they go to the homepage of the website. The code checks for such preference and replaces the URL shown by the browser accordingly and shows a User Account page (albeit minimal). This way, there will be no history record for the original homepage of the website, only for the User Account page.

``` js
if (localStorage["first-page"] === "account") {
 window.history.replaceState({"page": "account", "User Account", "/account"});
 document.body.innerHTML = "<h1>User Account</h1>";
}
```

