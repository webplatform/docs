{{Page_Title}}
{{Flags}}
{{Summary_Section|Refers to the current object.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= this.property}}
}}
{{Remarks_Section
|Remarks=The required property argument is one of the current object's properties

The this keyword can be used in object constructors to refer to the current object.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=In the following example, '''this''' refers to the newly created Car object, and assigns values to three properties:

|Code= function Car(color, make, model){
    this.color = color;
    this.make = make;
    this.model = model;
 }
}}{{Single_Example
|Language=JavaScript
|Description=The '''this''' keyword generally refers to the '''window''' object if used outside of the scope of any other object. However, inside event handlers this refers to the DOM element that raised the event.

In the following code (for Internet Explorer 9 and later), the event handler prints the string version of a button that has an ID of "clicker".

|Code= document.getElementById("clicker").addEventListener("click", eventHandler, false);
 
         function eventHandler(ev) {
             document.write(this.toString());
         }
 
 // Output (when you click the button): [object HTMLButtonElement]
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/operators/new{{!}}new Operator]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/w062xezx(v=vs.94).aspx
|HTML5Rocks_link=
}}