{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs examples.
|Checked_Out=No
|High-level issues=Stub, Needs Flags, Needs Review
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Gets or sets a textual representation of a CSS rule.}}
{{API_Object_Property
|Property_applies_to=css/cssom/CSSRule/CSSRule
|Read_only=No
|Example_object_name=rule
|Return_value_name=ruleText
|Javascript_data_type=String
|Return_value_description=Returns a textual representation of a CSS rule.
|Example_value_name=ruleText
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Code=<div id="myDiv">&nbsp;</div>
<input type="button" value="Blue" id="blueButton">
<input type="button" value="Red" id="redButton">
<script>
    redButton.onclick=function(){
        //create a css style using cssText
        myDiv.style.cssText = "background-image: radial-gradient(red,  yellow); color: darkred;"

        // write the cssText to the contents of the div
        myDiv.innerHTML = "The cssText value is: " + myDiv.style.cssText;
    }
    blueButton.onclick=function(){
        //create a css style using cssText
        myDiv.style.cssText = "background-image: radial-gradient(blue,  white); color: darkblue;"
			
        // write the cssText to the contents of the div
        myDiv.innerHTML = "The cssText value is: " + myDiv.style.cssText;
    }
</script>
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/css/cssText/cssText.html
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 2 Style
|URL=http://www.w3.org/TR/2000/REC-DOM-Level-2-Style-20001113/css.html
|Status=Recommendation
|Relevant_changes=Section 2.1
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=CSSOM
}}
{{Topics|API, CSS, CSS-Regions}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}