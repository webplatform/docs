{{Page_Title}}
{{Flags
|Checked_Out=No
|Editorial notes=New listing page with proper object capitalization; replaces '''window'''.
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The '''window''' object is the top level Javascript object in a page, and is the global scope for a browser tab.
Global Javascript variables appear in the window object, as well as several important objects such as [[dom/Document|Document]].
}}
{{API_Object
|Subclass_of=dom/EventTarget
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=This example displays an alert for the current window.
|Code=alert("A simple message.")
}}{{Single Example
|Language=JavaScript
|Code=if ( window.frames !{{=}} null ) {
    for ( i {{=}} 0; i &lt; window.frames.length; i++ )
        console.log("Child window " + i + " is named " + window.frames(i).name);
}
}}{{Single Example
|Language=HTML
|Description=This example shows a simple event handler function for the window's '''onload''' event. In the absence of a '''window''' element, the '''body''' element hosts the following window object events: '''onblur''', '''onbeforeunload''', '''onfocus''', '''onload''', and '''onunload'''.
|Code=&#60;body onload{{=}}"console.log('Document is loaded!');"&#62;
}}
}}
{{Notes_Section
|Notes=You can use the '''window''' object to retrieve information about the state of the window. You also can use this object to gain access to the document in the window, to the events that occur in the window, and to other factors that affect the window.
You can apply any window property, method, or collection to any variable or expression that evaluates to a '''window''' object, regardless of how that window was created. Additionally, you can access all window properties, methods, and collections in the current window by using the property, method, or collection name directly—that is, without prefixing it with an expression that evaluates to the current '''window''' object. However, to help make more readable code and to avoid potential ambiguities, many authors use the '''window''' keyword when accessing window properties, methods, and collections for the current window. This keyword always refers to the current window.
'''Note'''  The window's properties, methods, and collection names are reserved keywords and cannot be used as the names of variables or routines.
The following table lists pertinent information for some of the properties of the '''window''' object.
{{{!}} class="wikitable"
{{!}}-
!Property
!Method
!Description
{{!}}-
{{!}}'''opener'''
{{!}}'''open'''
{{!}}The '''opener''' property is available only from a document opened using the '''window.open''' method.
{{!}}-
{{!}}'''parent''', '''top'''
{{!}}None
{{!}}The '''parent''' and '''top''' properties are available for a window opened inside a '''frame''' or '''iframe'''. The two properties return the topmost parent and immediate parent, respectively.
{{!}}-
{{!}}'''parent''', '''top'''
{{!}}'''open'''
{{!}}The '''parent''' and '''top''' properties are available for a window opened via the '''open''' method or as a dialog and returns the current window.
{{!}}-
{{!}}'''length'''
{{!}}None
{{!}}Regardless of how the window is opened, the '''length''' property returns the number of frames in a window.
{{!}}-
{{!}}'''dialogArguments''', '''dialogHeight''', '''dialogLeft''', '''dialogTop''', '''dialogWidth''', '''returnValue'''
{{!}}'''showModalDialog''' and '''showModelessDialog'''
{{!}}These properties are available only for windows created using the two methods listed, '''showModalDialog''' and '''showModelessDialog'''
{{!}}}
 
Typically, the browser creates one '''window''' object when it opens an HTML document. However, if a document defines one or more frames (that is, contains one or more '''frame''' or '''iframe''' tags), the browser creates one '''window''' object for the original document and one additional '''window''' object for each frame. These additional objects are  of the original window and can be affected by actions that occur in the original. For example, closing the original window causes all child windows to close. You can also create new windows (and corresponding window objects) using methods such as '''open''', '''showModalDialog''', and '''showModelessDialog'''.
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
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
{{Concept_Listing
|Use_page_title=No
|List_all_subpages=No
}}