---
title: 'EntrySync'
notes:
  - 'Out of date; feature discontinued. See http://www.w3.org/TR/file-system-api/.'
readiness: 'Out of Date'
standardization_status: 'W3C Working Draft'
summary: "An abstract interface representing entries in a file system, each of which may be a File or DirectoryEntry.\n"
tags:
  0: API
  1: Objects
  3: FileSystemAPI
uri: apis/filesystem/EntrySync

---
## Summary

An abstract interface representing entries in a file system, each of which may be a File or DirectoryEntry.

**Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

## Properties

API Name
:   Summary

[filesystem](/apis/filesystem/EntrySync/filesystem)
:   The file system on which the EntrySync resides.

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

[fullPath](/apis/filesystem/EntrySync/fullPath)
:   The full absolute path from the root to the EntrySync.

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

[isDirectory](/apis/filesystem/EntrySync/isDirectory)
:   True if the EntrySync is a directory.

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

[isFile](/apis/filesystem/EntrySync/isFile)
:   True if the EntrySync is a file.

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

[name](/apis/filesystem/EntrySync/name)
:   The name of the EntrySync, excluding the path leading to it.

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

## Methods

API Name
:   Summary

[copyTo](/apis/filesystem/EntrySync/copyTo)
:   Copy an EntrySync to a different location on the file system.

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

[getMetadata](/apis/filesystem/EntrySync/getMetadata)
:   Look up metadata about this EntrySync.

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

[getParent](/apis/filesystem/EntrySync/getParent)
:   Look up the parent DirectoryEntrySync containing this EntrySync. If this EntrySync is the root of its filesystem, its parent is itself.

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

[moveTo](/apis/filesystem/EntrySync/moveTo)
:   Move an EntrySync to a different location on the file system.

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

[remove](/apis/filesystem/EntrySync/remove)
:   Deletes a file or directory.

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

[toURL](/apis/filesystem/EntrySync/toURL)
:   Returns a URL that can be used to identify this EntrySync.

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

## Events

*No events.*

## Related specifications

[W3C File API: Directories and System Specification](http://dev.w3.org/2009/dap/file-system/pub/FileSystem/)
:   W3C Working Draft
