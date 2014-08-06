{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|Returns the Function object being executed, that is, the body text of the specified Function object.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format=[ function '''.''' ] '''arguments.callee'''
}}
|Values=
}}
{{JS_Return_Value}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=function factorial(n){
   if (n &lt;= 0)
      return 1;
   else
      return n * arguments.callee( n - 1 ) }
 document.write(factorial(4));
}}
}}
{{Remarks_Section
|Remarks=The optional function argument is the name of the currently executing Function object.

The '''callee''' property is a member of the '''arguments''' object that becomes available only when the associated function is executing.

The initial value of the '''callee''' property is the Function object being executed. This allows anonymous functions to be recursive.
}}
{{Notes_Section}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Function/caller{{!}}caller Property (Function)]]
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/334e1zza(v=vs.94).aspx
|HTML5Rocks_link=
}}