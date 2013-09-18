{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Grid items that are not explicitly placed into a grid cell are automatically placed into an unoccupied grid cell. This property controls the direction in which the search for unoccupied cells takes place, and whether rows or columns are added as needed to accommodate the content.}}
{{CSS Property
|Initial value=none
|Applies to=Grid containers
|Inherited=No
|Media=visual
|Computed value=As specified
|Animatable=No
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=none
|Description=Rather than use the auto-placement algorithm, auto-placed grid items are positioned according to the grid-auto-position property.
}}{{CSS Property Value
|Data Type=rows
|Description=Causes items to be placed by filling each row in turn, adding new rows as necessary.
}}{{CSS Property Value
|Data Type=columns
|Description=Causes items to be placed by filling each column in turn, adding new columns as necessary.
}}{{CSS Property Value
|Data Type=dense
|Description=If specified, the auto-placement algorithm uses a "dense" packing algorithm approach, which attempts to fill in holes in the grid if smaller items come up later. (By contract, the default auto-placement algorithm packing approach is "sparse", which permanently skips spaces that it cannot fill with the current grid item.)

Note: This may cause items to appear out-of-order.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/*
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
}}{{Single Example
|Language=HTML
|Code=<form>
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

}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C Grid Layout Module
|URL=http://www.w3.org/TR/css3-grid-layout
|Status=W3C Working Draft
}}
}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}