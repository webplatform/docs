{{Page_Title}}
{{Flags}}
{{Summary_Section|Used by the [[javascript/JSON/stringify{{!}}JSON.stringify]] method to enable the transformation of an object's data for JavaScript Object Notation (JSON) serialization.

}}
{{JS_Syntax|Formats={{JS_Syntax_Format
|Format= objectname.'''toJSON()'''}}
|Values={{JS_Syntax_Parameter
|Name=objectname
|Required=Required
|Description=An object for which JSON serialization is wanted.}}
}}
{{Remarks_Section
|Remarks=The toJSON method is used by the JSON.stringify function.JSON.stringify serializes a JavaScript value into JSON text. If a toJSON method is provided to JSON.stringify , the toJSON method is called when JSON.stringify is called.

The toJSON method is a built-in member of the [[javascript/Date{{!}}Date]] JavaScript object. It returns an ISO-formatted date string for the UTC time zone (denoted by the suffix Z).

You can override the toJSON method for the Date type, or define a toJSON method for other object types to achieve transformation of data for the specific object type before JSON serialization.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Language=JavaScript
|Description=The following example uses the toJSON method to serialize string member values in uppercase. The toJSON method is called when JSON.stringify is called.

|Code= var contact = new Object();
 contact.firstname = "Jesper";
 contact.surname = "Aaberg";
 contact.phone = ["555-0100", "555-0120"];
 
 contact.toJSON = function(key)
  {
     var replacement = new Object();
     for (var val in this)
     {
         if (typeof (this[val]) === 'string')
             replacement[val] = this[val].toUpperCase();
         else
             replacement[val] = this[val]
     }
     return replacement;
 };
 
 var jsonText = JSON.stringify(contact);
 
 /* The value of jsonText is:
 '{"firstname":"JESPER","surname":"AABERG","phone":["555-0100","555-0120"]}'
 */
}}{{Single_Example
|Language=JavaScript
|Description=The following example illustrates how to use the toJSON method that is a built-in member of the [[javascript/Date{{!}}Date]] object.

|Code= var dt = new Date('8/24/2009');
 dt.setUTCHours(7, 30, 0);
 var jsonText = JSON.stringify(dt);
 
 /* The value of jsonText is:
 '"2009-08-24T07:30:00Z"'
 */
}}}}
{{See_Also_Section
|Manual_links=* [[javascript/JSON{{!}}JSON Object]]
* [[javascript/JSON/parse{{!}}JSON.parse Function]]
* [[javascript/JSON/stringify{{!}}JSON.stringify Function]]
* [[javascript/methods{{!}}JavaScript Methods]]
}}
{{Topics | JS Basic}}

{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/cc907896(v=vs.94).aspx
|HTML5Rocks_link=
}}