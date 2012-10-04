{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following examples use the '''deviceYDPI''' property to retrieve the vertical DPI of the screen.
|LiveURL=This example uses the '''deviceYDPI''' and '''logicalYDPI''' properties to calculate the vertical scale factor that Internet Explorer is applying.  The function in this example returns <code>1</code> if Internet Explorer is not adjusting the scale of the screen.
|Code=
&lt;script&gt;
  function fnScaleFactorY() {
    var nScaleFactor {{=}} screen.deviceYDPI / screen.logicalYDPI;
    return nScaleFactor;
  }
&lt;/script&gt;
}}
{{Single_Example
|Description=This example uses the [[css/selectors/zoom|'''-ms-zoom''']] property of the '''BODY''' element to adjust the scale of the document "manually" if Internet Explorer is not adjusting the scale of the screen and the user's vertical DPI is higher than normal. This is a simple but imprecise way to make a document look the same on higher resolution screens.  You can achieve finer control over the layout of your documents by modifying the properties of individual elements or groups of elements.
|LiveURL=
|Code=
&lt;script&gt;	
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
}}}}
{{Notes_Section
|Notes=
===Remarks===
On most systems, there is no difference between horizontal and vertical DPI.
The '''deviceYDPI''' property was introduced in Microsoft Internet Explorer 6.
For information about how Internet Explorer 6 and later can adjust the scale of the display on screens with higher-than-normal DPI, see Adjusting Scale for Higher DPI Screens.
|Import_Notes=
===Syntax===
===Standards information===
There are no standards that apply here.

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/screen|screen]]</code>
*<code>Reference</code>
*<code>[[css/cssom/screen/deviceXDPI|deviceXDPI]]</code>
*<code>logicalXDPI</code>
*<code>logicalYDPI</code>
|Topic_clusters=CSSOM
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}