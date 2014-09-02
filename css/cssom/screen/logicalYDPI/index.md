{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs spec reference, standardization status
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Retrieves the screen's vertical Dots Per Inch (DPI) value.}}
{{API_Object_Property
|Property_applies_to=css/cssom/screen
|Read_only=No
|Example_object_name=
|Return_value_name=
|Javascript_data_type=
|Return_value_description=
|Example_value_name=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following examples use the '''logicalYDPI''' property to retrieve the normal vertical DPI of the screen. The function in this example returns <code>1</code> if Internet Explorer is not adjusting the scale of the screen.
|Code=&lt;script&gt;
  function fnScaleFactorY() {
    var nScaleFactor {{=}} screen.deviceYDPI / screen.logicalYDPI;
    return nScaleFactor;
  }
&lt;/script&gt;
|LiveURL=
}}{{Single Example
|Language=JavaScript
|Description=This example uses the [[css/selectors/zoom|'''-ms-zoom''']] property of the '''BODY''' element to adjust the scale of the document "manually" if Internet Explorer is not adjusting the scale of the screen and the user's vertical DPI is higher than normal. This is a simple but imprecise way to make a document look the same on higher resolution screens.  You can achieve finer control over the layout of your documents by modifying the properties of individual elements or groups of elements.
|Code=&lt;script&gt;	
  // change layout on HighDPI screens when IE not scaling
  function fnScaleManually()
  {
    // normal DPI		
    var constNorm {{=}} 96; 
			
    // scaling is off and DPI higher than normal
    if ((screen.deviceYDPI {{=}}{{=}} screen.logicalYDPI) 
      &amp;&amp; (screen.deviceYDPI &gt; constNorm))
    {									
      document.body.style.zoom {{=}} 
        constNorm / screen.logicalYDPI;				
    }			
  }
&lt;/script&gt;
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
On most systems, there is no difference between horizontal and vertical DPI.  The normal DPI on most Windows systems is 96.
When Windows Internet Explorer is adjusting the scale of the screen, the value of this property does not equal the value of the '''deviceYDPI''' property.
'''logicalYDPI''' was introduced in Microsoft Internet Explorer 6.
For information about how Internet Explorer 6 and later can adjust the scale of the display on screens with higher-than-normal DPI, see Adjusting Scale for Higher DPI Screens.
|Import_Notes====Standards information===
There are no standards that apply here.
}}
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
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/screen|screen]]</code>
*<code>Reference</code>
*<code>[[css/cssom/screen/deviceXDPI|deviceXDPI]]</code>
*<code>deviceYDPI</code>
*<code>logicalXDPI</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}