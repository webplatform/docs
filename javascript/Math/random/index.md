{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Summary_Section|Returns a pseudorandom number between 0 and 1.}}
{{JS_Syntax
|Formats={{JS Syntax Format
|Format='''Math.random( ) '''
}}
|Values=
}}
{{JS_Return_Value
|Description=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=Math.random(); // 0.6236026335973293
Math.random(); // 0.10149288410320878
Math.random(); // 0.6313296002335846
|LiveURL=
}}
}}
{{Remarks_Section
|Remarks=The pseudo-random number generated is from 0 (inclusive) to 1 (exclusive), that is, the returned number can be zero, but it will always be less than one. The random number generator is seeded automatically when JavaScript is first loaded.

Due to the nature of the generation methods, these pseudo-random numbers are not uniformly distributed. They are normally distributed which means that, in general, a number is more likely to be closer to 0.5 than 0 or 1.

Note that this method is unsuitable for cryptography. The [https://dvcs.w3.org/hg/webcrypto-api/raw-file/tip/spec/Overview.html WebCrypto API] addresses this.
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{JS Object Listing}}
{{Topics | JS Basic}}
{{See_Also_Section
|Manual_links=* [[javascript/Math/pow{{!}}Math.pow Function]]
|External_links=
|Manual_sections=
}}
{{JS Topics
|JS Page Type=JS Basic
|Applies to=
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/yek4tbz0%28v=vs.94%29.aspx Windows Internet Explorer JavaScript reference
|HTML5Rocks_link=
}}