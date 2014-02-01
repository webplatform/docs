{{Page_Title}}
{{Flags}}
{{Summary_Section|Returns the Function object being executed, that is, the body text of the specified Function object.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= [ function '''.''' ] '''arguments.callee'''}}
}}
{{Remarks_Section
|Remarks=The optional function argument is the name of the currently executing Function object.

The '''callee''' property is a member of the '''arguments''' object that becomes available only when the associated function is executing.

The initial value of the '''callee''' property is the Function object being executed. This allows anonymous functions to be recursive.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Code= function factorial(n){
   if (n &lt;= 0)
      return 1;
   else
      return n * arguments.callee( n - 1 ) }
 document.write(factorial(4));
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/Function/caller{{!}}caller Property (Function)]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/334e1zza(v=vs.94).aspx
|HTML5Rocks_link=
}}