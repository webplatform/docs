{{Page_Title|applet – obsolete}}
{{Flags
|State=Not Ready
|Editorial notes=Deletion Candidate: It's deprecated, http://www.w3.org/TR/html5/obsolete.html#non-conforming-features
|Checked_Out=No
}}
{{Standardization_Status|Deprecated}}
{{API_Name|applet}}
{{Summary_Section|'''&lt;applet&gt;'''はJavaアプレットをウェブページに埋め込む際に使用します。}}
{{Markup_Element
|DOM_interface=dom/HTMLAppletElement
|Content='''&lt;applet&gt;'''要素はHTML4.01で非推奨となり、''HTML5の登場でほとんど使われなくなりました''。
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=以下はウェブページに「myApplet」というJavaアプレットを埋め込む例です。
|Code=<applet code="myApplet.class" width="500" height="500">
My Java applet goes here! 
</applet>
}}
}}
{{Notes_Section
|Notes====備考===
'''&lt;applet&gt;'''要素でJavaアプレットを実行する場合、ユーザのPCにJavaランタイム環境（JRE)がインストールされている必要があります。
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/REC-html40/struct/objects.html#h-13.4
|Status=W3C Recommendation
|Relevant_changes=Feature marked as deprecated
}}{{Related Specification
|Name=HTML5
|URL=http://www.w3.org/TR/html5/obsolete.html#the-applet-element
|Status=W3C Candidate Recommendation
|Relevant_changes=Feature marked as obsolete
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=8+
|Note=Windows Internet Explorer 8 and later. The value of the [[html/attributes/codeBase|'''codeBase''']] attribute depends on the current document compatibility mode.
}}
}}
{{See_Also_Section}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}