{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Content=Examples Needed
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Shorthand for setting all the explicit grid properties ([[css/properties/grid-template-rows|grid-template-rows]], [[css/properties/grid-template-columns|grid-template-columns]], and [[css/properties/grid-template-areas|grid-template-areas]]), as well as all the implicit grid properties ([[css/properties/grid-auto-rows|grid-auto-rows]], [[css/properties/grid-auto-columns|grid-auto-columns]], and [[css/properties/grid-auto-flow|grid-auto-flow]]), in a single declaration. If the <grid-auto-rows> value is omitted, it is set to the value specified for grid-auto-columns. Other omitted values are set to their initial values.}}
{{CSS Property
|Initial value=See individual properties
|Applies to=Grid containers
|Inherited=No
|Media=visual
|Computed value=See individual properties
|Animatable=No
|CSS percentages=See individual properties
|Values={{CSS Property Value
|Data Type=<grid-template>
|Description=Itself a shorthand property, see [[css/properties/grid-template|grid-template]] for details.
}}{{CSS Property Value
|Data Type=<grid-auto-flow>
|Description=See [[css/properties/grid-auto-flow|grid-auto-flow]] for details.
}}{{CSS Property Value
|Data Type=<grid-auto-columns> / <grid-auto-rows>
|Description=See [[css/properties/grid-auto-columns|grid-auto-columns]] and [[css/properties/grid-auto-rows|grid-auto-rows]] for details.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=1 column grid
|Code=<div class="grid">
  <!-- 100% wide -->
</div>


}}{{Single Example
|Language=CSS
|Description=2 column grid
|Code=<div class="grid">
  <div class="col-2-3">
     Main Content
  </div>
  <div class="col-1-3">
     Sidebar
  </div>
</div>
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
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