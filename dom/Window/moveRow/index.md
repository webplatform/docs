---
title: moveRow
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
  - API
  - Object
  - Methods
  - DOM
uri: dom/Window/moveRow

---
## <span>Summary</span>

Moves a table row to a new position.

Method of [dom/Window](/dom/Window)[dom/Window](/dom/Window)

## <span>Syntax</span>

``` js
 oTable.moveRow(/* see parameter list */);
```

## <span>Parameters</span>

### <span>indexFrom</span>

 Data-type
:   Number

**Integer** that specifies the index in the [**rows**](/dom/HTMLElement/rows) collection of the table row that is moved. -1 Default.

### <span>indexTo</span>

 Data-type
:   Number

**Integer** that specifies where the row is moved within the [**rows**](/dom/HTMLElement/rows) collection. -1 Default.

## <span>Return Value</span>

No return value

## <span>Examples</span>

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

## <span>Usage</span>

     Use to re-order rows of tabula data.

## <span>Notes</span>

### <span>Remarks</span>

Rows between the *indexFrom* and *indexTo* positions in the [**rows**](/dom/HTMLElement/rows) collection are shifted based on the direction the row moves.