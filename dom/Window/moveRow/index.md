---
title: 'moveRow'
attributions:
  - 'Microsoft Developer Network: [[moveRow Method](http://msdn.microsoft.com/en-us/library/ie/ms536622(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Window
    href: /dom/Window
standardization_status: Non-Standard
summary: 'Moves a table row to a new position.'
tags:
  - API_Object_Methods
  - DOM
uri: dom/Window/moveRow

---
## Summary

Moves a table row to a new position.

Method of [dom/Window](/dom/Window)[dom/Window](/dom/Window)

## Syntax

``` js
 oTable.moveRow(/* see parameter list */);
```

## Parameters

### indexFrom

 Data-type
:   Number

**Integer** that specifies the index in the [**rows**](/dom/HTMLElement/rows) collection of the table row that is moved. -1 Default.

### indexTo

 Data-type
:   Number

**Integer** that specifies where the row is moved within the [**rows**](/dom/HTMLElement/rows) collection. -1 Default.

## Return Value

No return value

## Examples

This example uses the **moveRow** method to exchange the first and second rows in a table when the user clicks a button.

``` js
<script type="text/javascript>
function fnMove(){
   oTable.moveRow(0,1);
}
</script>
<input type="button" value="Change Rows" onclick="fnMove()">
<table id="oTable">
<tr><td>Cell 1, Row 1</td></tr>
<tr><td>Cell 1, Row 2</td></tr>
</table>
```

## Usage

     Use to re-order rows of tabula data.

## Notes

### Remarks

Rows between the *indexFrom* and *indexTo* positions in the [**rows**](/dom/HTMLElement/rows) collection are shifted based on the direction the row moves.
