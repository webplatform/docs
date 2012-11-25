{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=In a hosting scenario, the object model is defined by the application hosting the Internet Explorer components (refer to the hosting application for documentation). For more information about how to implement extensions to the Dynamic HTML (DHTML) object model, see About the Browser.
This object is not supported in HTML Applications.
|Import_Notes====Additional Members (MSDN)===
The '''external''' object has these types of members:
[[#Additional_Methods|Additional Methods]]
[[#Additional_Properties|Additional Properties]]


====Additional Methods====
The '''external''' object has these methods.
{{{!}} class="wikitable"
{{!}}-
!Method
!Description
{{!}}-
{{!}}'''AddChannel'''
{{!}}Obsolete. Presents a dialog box that enables the user to add the specified channel, or to change the channel URL, if it is already installed.

This method is not supported for Metro style apps using JavaScript.
{{!}}-
{{!}}'''AddDesktopComponent'''
{{!}}Obsolete.  Adds a Web site or image to the Active Desktop.

This method is not supported for Metro style apps using JavaScript.
{{!}}-
{{!}}'''AddFavorite'''
{{!}}Deprecated.  Prompts the user with a dialog box to add the specified URL to the '''Favorites''' list. 

This method is not supported for Metro style apps using JavaScript.
{{!}}-
{{!}}'''AddSearchProvider'''
{{!}}Deprecated. Adds a search provider to the registry.

This method is not supported for Metro style apps using JavaScript.
{{!}}-
{{!}}'''AddService'''
{{!}}Deprecate. User initiated action to add a service.

This method is not supported for Metro style apps using JavaScript.
{{!}}-
{{!}}'''AddToFavoritesBar'''
{{!}}Deprecated. Adds
a URL to the '''Favorites Bar'''.

This method is not supported for Metro style apps using JavaScript.
{{!}}-
{{!}}[[dom/methods/AutoCompleteSaveForm|'''AutoCompleteSaveForm''']]
{{!}}Saves the specified form in the AutoComplete data store.

This method is not supported for Metro style apps using JavaScript.
{{!}}-
{{!}}[[dom/methods/AutoScan|'''AutoScan''']]
{{!}}No longer available as of Internet Explorer 7. Attempts to connect to a Web server by passing the specified query through completion templates. 

This method is not supported for Metro style apps using JavaScript.
{{!}}-
{{!}}'''bubbleEvent'''
{{!}}Propagates an event up its containment hierarchy.
{{!}}-
{{!}}[[dom/methods/ContentDiscoveryReset|'''ContentDiscoveryReset''']]
{{!}}Resets the list of feeds, search providers, and Web Slices associated with the page.

This method is not supported for Metro style apps using JavaScript.
{{!}}-
{{!}}'''ImportExportFavorites'''
{{!}}Deprecated. Handles the import and export of Internet Explorer favorites.

This method is not supported for Metro style apps using JavaScript.
{{!}}-
{{!}}[[dom/methods/InPrivateFilteringEnabled|'''InPrivateFilteringEnabled''']]
{{!}}Detects whether the user has enabled InPrivate Filtering.

This method is not supported for Metro style apps using JavaScript.
{{!}}-
{{!}}'''IsSearchProviderInstalled'''
{{!}}Deprecated. Determines if a search provider has been installed for the current user and whether it is set as default.

This method is not supported for Metro style apps using JavaScript.
{{!}}-
{{!}}'''IsServiceInstalled'''
{{!}}Deprecated. Check if a service is already installed.
{{!}}-
{{!}}'''IsSubscribed'''
{{!}}Obsolete. Retrieves a value indicating whether the client subscribes to the given channel.

This method is not supported for Metro style apps using JavaScript.
{{!}}-
{{!}}[[dom/methods/msActiveXFilteringEnabled|'''msActiveXFilteringEnabled''']]
{{!}}Determines whether ActiveX Filtering is enabled by the user.

This method is not supported for Metro style apps using JavaScript.
{{!}}-
{{!}}'''msAddSiteMode'''
{{!}}Creates a pinned site shortcut to the current webpage on the Windows Start menu.

This method is not supported for Metro style apps using JavaScript.
{{!}}-
{{!}}[[dom/methods/msAddTrackingProtectionList|'''msAddTrackingProtectionList''']]
{{!}}Adds an external Tracking Protection list. 

This method is not supported for Metro style apps using JavaScript.
{{!}}-
{{!}}'''msIsSiteMode'''
{{!}}Determines whether the current page was launched as a pinned site.
{{!}}-
{{!}}'''msIsSiteModeFirstRun'''
{{!}}Determines whether a pinned site was launched for the first time.
{{!}}-
{{!}}[[dom/methods/msProvisionNetworks|'''msProvisionNetworks''']]
{{!}}Attempts to configure a connection profile using credentials specified in an XML document.
{{!}}-
{{!}}[[dom/methods/msReportSafeUrl|'''msReportSafeUrl''']]
{{!}}Reports the current URL as a safe URL.
{{!}}-
{{!}}'''msSiteModeActivate'''
{{!}}Flashes the pinned site taskbar button. 

This method is not supported for Metro style apps using JavaScript.
{{!}}-
{{!}}'''msSiteModeAddButtonStyle'''
{{!}}Defines an alternate icon image and tooltip for the specified button. 

This method is not supported for Metro style apps using JavaScript.
{{!}}-
{{!}}'''msSiteModeAddJumpListItem'''
{{!}}Adds a new entry to the Jump List of a taskbar button.
{{!}}-
{{!}}'''msSiteModeAddThumbBarButton'''
{{!}}Adds a button to the Thumbnail Toolbar.

This method is not supported for Metro style apps using JavaScript.
{{!}}-
{{!}}'''msSiteModeClearBadge'''
{{!}}Clears the notifications on a pinned site badge in Windows 8.
{{!}}-
{{!}}'''msSiteModeClearIconOverlay'''
{{!}}Removes the icon overlay from the taskbar button. 

This method is not supported for Metro style apps using JavaScript.
{{!}}-
{{!}}'''msSiteModeClearJumpList'''
{{!}}Deletes the Jump List.
{{!}}-
{{!}}'''msSiteModeCreateJumpList'''
{{!}}Creates a new group of items on the Jump List.
{{!}}-
{{!}}'''msSiteModeRefreshBadge'''
{{!}}Causes  Windows 8 to refresh the site tile badge for a webpage to be sure that it is up to date.
{{!}}-
{{!}}'''msSiteModeSetIconOverlay'''
{{!}}Adds an icon overlay to the pinned site taskbar button.

This method is not supported for Metro style apps using JavaScript.
{{!}}-
{{!}}'''msSiteModeShowButtonStyle'''
{{!}}Changes the icon image and tooltip of a Thumbnail Toolbar button. 

This method is not supported for Metro style apps using JavaScript.
{{!}}-
{{!}}'''msSiteModeShowJumpList'''
{{!}}Shows updates to the list of items in a Jump List.
{{!}}-
{{!}}'''msSiteModeShowThumbBar'''
{{!}}Enables the Thumbnail Toolbar in the thumbnail preview of a pinned site. 

This method is not supported for Metro style apps using JavaScript.
{{!}}-
{{!}}'''msSiteModeUpdateThumbBarButton'''
{{!}}Changes the state of a Thumbnail Toolbar button. 

This method is not supported for Metro style apps using JavaScript.
{{!}}-
{{!}}[[dom/methods/msTrackingProtectionEnabled|'''msTrackingProtectionEnabled''']]
{{!}}Determines whether any Tracking Protection lists are enabled by the user. 

This method is not supported for Metro style apps using JavaScript.
{{!}}-
{{!}}'''NavigateAndFind'''
{{!}}Navigates to the specified URL and selects the specified text.

This method is not supported by Metro style apps using JavaScript.

Navigates to the specified URL and selects the specified text.
{{!}}-
{{!}}'''raiseEvent'''
{{!}}Triggers an event, as specified.
{{!}}-
{{!}}'''setContextMenu'''
{{!}}Constructs a context menu, as specified.
{{!}}-
{{!}}[[dom/methods/ShowBrowserUI|'''ShowBrowserUI''']]
{{!}}Opens the specified browser dialog box.

This method is not supported for Metro style apps using JavaScript.
{{!}}}
 

====Additional Properties====
The '''external''' object has these properties.
{{{!}} class="wikitable"
{{!}}-
!Property
!Description
{{!}}-
{{!}}'''menuArguments'''
{{!}}Returns the window object in which the context menu item opened.


This property is not supported for Metro style apps using JavaScript.
{{!}}-
{{!}}'''onvisibilitychange'''
{{!}}Sets or retrieves a value on visibility change.
{{!}}-
{{!}}'''scrollbar'''
{{!}}Sets or retrieves whether to show the scrollbar.
{{!}}-
{{!}}'''selectableContent'''
{{!}}Sets or retrieves whether selectable content is valid.
{{!}}-
{{!}}'''version'''
{{!}}Retrieves a string representing the version in the format "N.nnnn platform", where N is an integer representing the major version number, nnnn is a number of characters representing the minor version number, and platform is the platform (win32, mac, alpha, and so on).
{{!}}-
{{!}}'''visibility'''
{{!}}Retrieves whether content is visible.
{{!}}}
 
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