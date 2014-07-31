{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Returns whether a value is greater than the '''max''' attribute on an input control.}}
{{API_Object_Property
|Property_applies_to=dom/ValidityState
|Read_only=Yes
|Example_object_name=element.validity
|Return_value_name=result
|Javascript_data_type=Boolean
|Return_value_description=Whether a value is greater than the '''max''' attribute on an input control.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example validates a numeric (type="number") input field on the onblur event handler. If a number outside the range values of the input control is entered the custom validity message is displayed when the form is submitted.
|Code=<syntaxHighlight lang="html5">
<form>
<div class="form-group">
  <label for="ex_nbr4to20">Enter a number between 4 and 20</label>
  <input id="ex_nbr4to20" name="ex[nbr4to20]" class="form-control" type="number" required  min="4" max="20" step="2" placeholder="e.g. 6">
</div>
<input type="submit" value="Try Submitting" />
</form>
<script>
  var fieldElement=document.getElementById('ex_nbr4to20');
  function onBlurHandler(event){
    var field = event.target;
    console.log(field.validity, field.validity.rangeOverflow);
    if(!!field.validity) {
      if(!!field.validity.rangeOverflow){
        // Try setting a range over 20
        field.setCustomValidity("The number is outside of an acceptable range");
      } else {
        field.setCustomValidity(""); // Has to be an empty string
      }
    } else {
      // Legacy validation
    }
    //console.log(field.validity);
  }
  fieldElement.addEventListener('blur', onBlurHandler, false);
</script>
</syntaxHighlight>
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C HTML5
|URL=http://www.w3.org/TR/html5/
|Status=Working Draft
|Relevant_changes=Section 4.10.21.3
}}{{Related Specification
|Name=WHATWG HTML
|URL=http://www.whatwg.org/specs/web-apps/current-work/multipage
|Status=Living Standard
|Relevant_changes=Section 4.10.21.3
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN, HTML5Rocks
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh773357(v=vs.85).aspx rangeOverflow Property]
|HTML5Rocks_link=[http://www.html5rocks.com/en/tutorials/forms/html5forms/ Making forms fabulous]
}}
}





}