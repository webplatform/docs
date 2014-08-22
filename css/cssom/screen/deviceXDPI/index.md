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
{{Summary_Section|Retrieves the device's horizontal Dots Per Inch (DPI) value.}}
{{API_Object_Property
|Property_applies_to=css/cssom/screen
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following examples use the '''deviceXDPI''' property to retrieve the horizontal DPI of the screen. The function in this example returns <code>1</code> if Internet Explorer is not adjusting the scale of the screen.
|Code=&lt;script&gt;
  function fnScaleFactorX() {
    var nScaleFactor {{=}} screen.deviceXDPI / screen.logicalXDPI;
    return nScaleFactor;
  }
&lt;/script&gt;
}}{{Single Example
|Language=JavaScript
|Description=This example uses the [[css/selectors/zoom|'''-ms-zoom''']] property of the '''BODY''' element to adjust the scale of the page "manually" if Internet Explorer is not adjusting the scale of the screen and the user's horizontal DPI is higher than normal. This is a simple but imprecise way to make a document look the same on higher resolution screens.  You can achieve finer control over the layout of your documents by modifying the properties of individual elements or groups of elements.
|Code=&lt;script&gt;	
  // change layout on HighDPI screens when IE not scaling
  function fnScaleManually()
  {
    // normal DPI		
    var constNorm {{=}} 96; 
			
    // scaling is off and DPI higher than normal
    if ((screen.deviceXDPI {{=}}{{=}} screen.logicalXDPI) 
      &amp;&amp; (screen.deviceXDPI &gt; constNorm))
    {									
      document.body.style.zoom {{=}} 
        constNorm / screen.logicalXDPI;				
    }			
  }
&lt;/script&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
On most systems, there is no difference between horizontal and vertical DPI.
The 
'''deviceXDPI''' property was introduced in Microsoft Internet Explorer 6.
For information about how Internet Explorer 6 and later can adjust the scale of the display on screens with higher-than-normal DPI, see Adjusting Scale for Higher DPI Screens.
|Import_Notes====Syntax===
===Standards information===
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
|Topic_clusters=CSSOM
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/screen|screen]]</code>
*<code>Reference</code>
*<code>deviceYDPI</code>
*<code>logicalXDPI</code>
*<code>logicalYDPI</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}