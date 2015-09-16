---
title: Boolean
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/t7bkhaz6(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Creates a new Boolean (true/false) value.'
tags:
  0: JS
  1: Basic
  3: Object
uri: javascript/Boolean

---
## Summary

Creates a new Boolean (true/false) value.

## Syntax

<span class="language">JavaScript</span>

    new Boolean ([ boolValue ])

<span class="language">JavaScript</span>

    ([ boolValue ])

**boolValue**
:   Required. The initial Boolean value for the new object. Possible values are true and false.

Other values (like 1 and 0) are converted to a Boolean expression.

## Return Value

If the boolean value is omitted, or is false , 0, null , NaN , or an empty string, Boolean returns false. Otherwise, it returns true true.

## Examples

Using Boolean to define a test condition

``` js
var x = new Boolean(false);
// This value can also be expressed as x = false;
if (x) {
  // . . . this code will not be executed
}
```

Using implicit Boolean constructor

``` js
// Implicit use of new Boolean(true)
var IsLoggedIn = true;
if (isLoggedIn) {
  // actions that are only done when isLoggedIn is true
}
```

## Remarks

The **Boolean** object is a wrapper for the Boolean data type. JavaScript implicitly uses the **Boolean** object whenever a Boolean data type is converted to a **Boolean** object.

You rarely instantiate the **Boolean** object explicitly.

## Properties

The following table lists the properties of the **Boolean** object.

|Property|Summary|
|:-------|:------|
|[prototype](/javascript/Boolean/prototype)|Returns a reference to the prototype for a Boolean.|

## Functions

The following table lists the functions of the **Boolean** object.

## Methods

The following table lists the methods of the **Boolean** object.

|Method|Summary|
|:-----|:------|
|[constructor](/javascript/Boolean/constructor)|Initializes a Boolean object.|
|[toString](/javascript/Boolean/toString)|Returns a string representation of a Boolean object.|

## See also

### Specification

[Boolean Objects](http://www.ecma-international.org/ecma-262/5.1/#sec-15.6) ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

