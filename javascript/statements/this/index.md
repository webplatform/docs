{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs spec reference, standardization status
|Checked_Out=No
}}
{{Summary_Section|Refers to the current object.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=this.property
}}
|Values=
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=In the following example, '''this''' refers to the newly created Car object, and assigns values to three properties:
|Code=function Car(color, make, model){
    this.color = color;
    this.make = make;
    this.model = model;
 }
}}{{Single Example
|Language=JavaScript
|Description=The '''this''' keyword generally refers to the '''window''' object if used outside of the scope of any other object. However, inside event handlers this refers to the DOM element that raised the event.

In the following code (for Internet Explorer 9 and later), the event handler prints the string version of a button that has an ID of "clicker".
|Code=document.getElementById("clicker").addEventListener("click", eventHandler, false);
 
         function eventHandler(ev) {
             document.write(this.toString());
         }
 
 // Output (when you click the button): [object HTMLButtonElement]
}}
}}
{{Remarks_Section
|Remarks=The required property argument is one of the current object's properties

The this keyword can be used in object constructors to refer to the current object.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/operators/new{{!}}new Operator]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/w062xezx(v=vs.94).aspx
|HTML5Rocks_link=
}}