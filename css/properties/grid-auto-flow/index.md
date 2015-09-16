---
title: grid-auto-flow
notes:
  - 'Add description, compatibility.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`none`'
  'Applies to': 'Grid containers'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: N/A
readiness: 'In Progress'
standardization_status: 'W3C Working Draft'
summary: 'Automatically places grid elements into the grid layout if an explicit location is not designated.  Designates the direction of the the flow and whether rows or columns must be added to accommodate the element.'
tags:
  - CSS
  - Properties
uri: css/properties/grid-auto-flow

---
## Summary

Automatically places grid elements into the grid layout if an explicit location is not designated. Designates the direction of the the flow and whether rows or columns must be added to accommodate the element.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `none`

Applies to
:   Grid containers

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   As specified

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

Percentages
:   N/A

## Syntax

-   `grid-auto-flow: columns`
-   `grid-auto-flow: dense`
-   `grid-auto-flow: none`
-   `grid-auto-flow: rows`
-   `grid-auto-flow: sparse`

## Values

none
:   Causes auto-placed grid items to be placed according to the grid-auto-position property, rather than using the auto-placement algorithm.

rows
:   Fills each row in turn, adding new rows as necessary.

columns
:   Fills each column in turn, adding new columns as necessary.

dense
:   Uses a "dense" packing algorithm approach to fill in holes in the grid as smaller items appear.

Note: This may cause items to appear out-of-order.

sparse
:   Permanently skips cells that are not filled with the current item. The default auto-pacement algorithm packing approach.

## Examples

``` css
/*
In this form layout example, there are three columns, each auto-sized to their
contents. No rows are explicitly defined. The grid-auto-flow property is set to "rows",
which instructs the grid to search the rows first (that is, across the columns),
starting with the first row and adding rows as needed until sufficient space
is located to accommodate the position of any auto-placed grid item.
If the grid-auto-flow property is set to "columns", this instructs the grid to instead
search the columns first (that is, down the rows), starting with the first column
and adding columns as needed until sufficient space is located to accommodate
the position of any auto-placed grid item, resulting in a significantly different
object sequence within the grid.
*/
<style type="text/css">
  form {
    display: grid;
    /* Define three columns, all content-sized,
       and name the corresponding lines. */
    grid-template-columns: (labels) auto (controls) auto (oversized) auto;
    grid-auto-flow: rows;
  }
  form > label {
    /* Place all labels in the "labels" column and
       automatically find the next available row. */
    grid-column: labels;
    grid-row: auto;
  }
  form > input, form > select {
    /* Place all controls in the "controls" column and
       automatically find the next available row. */
    grid-column: controls;
    grid-row: auto;
  }

  #department {
    /* Auto place this item in the "oversized" column
       in the first row where an area that spans three rows
       won’t overlap other explicitly placed items or areas
       or any items automatically placed prior to this area. */
    grid-column: oversized;
    grid-row: span 3;
  }

  /* Place all the buttons of the form
     in the explicitly defined grid area. */
  #buttons {
    grid-row: auto;

    /* Ensure the button area spans the entire grid element
       in the row axis. */
    grid-column: 1 / -1;
    text-align: end;
  }
</style>
```

``` html
<form>
  <label for="firstname">First name:</label>
  <input type="text" id="firstname" name="firstname" />
  <label for="lastname">Last name:</label>
  <input type="text" id="lastname" name="lastname" />
  <label for="address">Address:</label>
  <input type="text" id="address" name="address" />
  <label for="address2">Address 2:</label>
  <input type="text" id="address2" name="address2" />
  <label for="city">City:</label>
  <input type="text" id="city" name="city" />
  <label for="state">State:</label>
  <select type="text" id="state" name="state">
    <option value="WA">Washington</option>
  </select>
  <label for="zip">Zip:</label>
  <input type="text" id="zip" name="zip" />

  <div id="department">
    <label for="department">Department:</label>
    <select id="department" name="department" multiple>
      <option value="finance">Finance</option>
      <option value="humanresources">Human Resources</option>
      <option value="marketing">Marketing</option>
    </select>
  </div>

  <div id="buttons">
    <button id="cancel">Cancel</button>
    <button id="back">Back</button>
    <button id="next">Next</button>
  </div>
</form>
```

## Related specifications

[W3C Grid Layout Module](http://www.w3.org/TR/css3-grid-layout)
:   W3C Working Draft
