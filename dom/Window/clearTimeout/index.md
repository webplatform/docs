{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Cancels a time-out that was set with the setTimeout method. }}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=timerID
|Data type=Number
|Description='''Integer''' that specifies the time-out setting returned by a previous call to the [[dom/Window/setTimeout|'''setTimeout''']] method.
|Optional=No
}}
|Method_applies_to=dom/Window
|Example_object_name=window
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=var alarm {{=}} {
  remind: function(aMessage) {
    alert(aMessage);
    delete this.timeoutID;
  },

  setup: function() {
    this.cancel();
    var self {{=}} this;
    this.timeoutID {{=}} window.setTimeout(function(msg) {self.remind(msg);}, 1000, "Wake up!");
  },

  cancel: function() {
    if(typeof this.timeoutID {{=}}{{=}} "number") {
      window.clearTimeout(this.timeoutID);
      delete this.timeoutID;
    }
  }
};
window.onclick {{=}} function() { alarm.setup() };
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
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Window.clearTimeout clearTimeout]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms536357(v=vs.85).aspx clearTimeout Method]
|HTML5Rocks_link=
}}