---
title: media
tags:
  - Markup
  - Elements
  - HTML
readiness: 'Not Ready'
notes:
  - 'Deletion Candidate'
summary: 'Presents audio or video data to the user. The media element provides the audio and video objects which are used to play sound and video content.'
uri: html/elements/media
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/events/abort
    - dom/events/blur
    - dom/events/change
    - dom/events/drag
    - dom/events/dragend
    - dom/events/dragenter
    - dom/events/dragleave
    - dom/events/dragover
    - dom/events/drop
    - dom/events/error
    - dom/events/focus
    - dom/events/input
    - dom/events/reset
    - dom/events/scroll
    - dom/events/selectstart
    - apis/audio-video/methods/canPlayType
    - dom/methods/compareDocumentPosition
    - dom/methods/getAttributeNodeNS
    - dom/attributes
    - dom/methods/getAttributeNS
    - dom/methods/getElementsByClassName
    - dom/properties/className
    - dom/methods/getElementsByTagNameNS
    - dom/methods/hasAttributeNS
    - dom/methods/isDefaultNamespace
    - dom/methods/isEqualNode
    - dom/methods/isSameNode
    - dom/methods/isSupported
    - apis/audio-video/methods/load
    - dom/methods/lookupNamespaceURI
    - dom/methods/lookupPrefix
    - dom/methods/matchesSelector
    - apis/audio-video/methods/pause
    - apis/audio-video/properties/paused
    - apis/audio-video/methods/play
    - dom/methods/removeAttributeNS
    - dom/methods/setAttributeNodeNS
    - dom/methods/setAttributeNS
    - apis/audio-video/properties/audioTracks
    - apis/audio-video/properties/autobuffer
    - apis/audio-video/properties/preload
    - apis/audio-video/properties/autoplay
    - apis/audio-video/properties/buffered
    - apis/audio-video/properties/controls
    - apis/audio-video/properties/currentSrc
    - apis/audio-video/properties/currentTime
    - apis/audio-video/properties/defaultPlaybackRate
    - apis/audio-video/properties/duration
    - apis/audio-video/properties/ended
    - apis/audio-video/properties/error
    - apis/audio-video/properties/initialTime
    - dom/properties/localName
    - apis/audio-video/properties/loop
    - apis/audio-video/properties/muted
    - dom/properties/namespaceURI
    - apis/audio-video/properties/networkState
    - apis/audio-video/properties/playbackRate
    - apis/audio-video/properties/played
    - apis/audio-video/HTMLTimeRanges
    - dom/properties/prefix
    - apis/audio-video/properties/seekable
    - apis/audio-video/properties/seeking
    - apis/audio-video/properties/src
    - dom/properties/textContent
    - apis/audio-video/properties/volume

---
# media

## Summary

Presents audio or video data to the user. The media element provides the audio and video objects which are used to play sound and video content.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLElement](/dom/HTMLElement)

**Needs Examples**: This section should include examples.

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 4.8.10

### Members

The **media** object has these types of members:

-   [\#events Events]
-   [\#methods Methods]
-   [\#properties Properties]

#### Events

The **media** object has these events.

Event
:   Description
[**onabort**](/w/index.php?title=dom/events/abort&action=edit&redlink=1)
:   Fires when the user aborts the download.
[**onblur**](/w/index.php?title=dom/events/blur&action=edit&redlink=1)
:   Fires when the object loses the input focus.
[**onchange**](/w/index.php?title=dom/events/change&action=edit&redlink=1)
:   Fires when the contents of the object or selection have changed.
[**ondrag**](/w/index.php?title=dom/events/drag&action=edit&redlink=1)
:   Fires on the source object continuously during a drag operation.
[**ondragend**](/w/index.php?title=dom/events/dragend&action=edit&redlink=1)
:   Fires on the source object when the user releases the mouse at the close of a drag operation.
[**ondragenter**](/w/index.php?title=dom/events/dragenter&action=edit&redlink=1)
:   Fires on the target element when the user drags the object to a valid drop target.
[**ondragleave**](/w/index.php?title=dom/events/dragleave&action=edit&redlink=1)
:   Fires on the target object when the user moves the mouse out of a valid drop target during a drag operation.
[**ondragover**](/w/index.php?title=dom/events/dragover&action=edit&redlink=1)
:   Fires on the target element continuously while the user drags the object over a valid drop target.
[**ondrop**](/w/index.php?title=dom/events/drop&action=edit&redlink=1)
:   Fires on the target object when the mouse button is released during a drag-and-drop operation.
[**onerror**](/w/index.php?title=dom/events/error&action=edit&redlink=1)
:   Fires when an error occurs during object loading.
[**onfocus**](/w/index.php?title=dom/events/focus&action=edit&redlink=1)
:   Fires when the object receives focus.
[**oninput**](/w/index.php?title=dom/events/input&action=edit&redlink=1)
:   Occurs when the text content of an element is changed through the user interface.
[**onload**](/dom/events/load)
:   Fires immediately after the client loads the object.
[**onreset**](/w/index.php?title=dom/events/reset&action=edit&redlink=1)
:   Fires when the user resets a form.
[**onscroll**](/w/index.php?title=dom/events/scroll&action=edit&redlink=1)
:   Fires when the user repositions the scroll box in the scroll bar on the object.
[**onselect**](/w/index.php?title=dom/events/selectstart&action=edit&redlink=1)
:   Fires when the current selection changes.

Â

#### Methods

The **media** object has these methods.

Method
:   Description
[**canPlayType**](/w/index.php?title=apis/audio-video/methods/canPlayType&action=edit&redlink=1)
:   Returns a string that specifies whether the client can play a given media resource type.
[**compareDocumentPosition**](/w/index.php?title=dom/methods/compareDocumentPosition&action=edit&redlink=1)
:   Compares the position of two nodes in a document.
[**getAttributeNodeNS**](/w/index.php?title=dom/methods/getAttributeNodeNS&action=edit&redlink=1)
:   Gets an [**attribute**](/w/index.php?title=dom/attributes&action=edit&redlink=1) object that matches the specified namespace and name.
[**getAttributeNS**](/w/index.php?title=dom/methods/getAttributeNS&action=edit&redlink=1)
:   Gets the value of the specified attribute within the specified namespace.
[**getElementsByClassName**](/w/index.php?title=dom/methods/getElementsByClassName&action=edit&redlink=1)
:   Gets a collection of objects that are based on the value of the [**CLASS**](/w/index.php?title=dom/properties/className&action=edit&redlink=1) attribute.
[**getElementsByTagNameNS**](/w/index.php?title=dom/methods/getElementsByTagNameNS&action=edit&redlink=1)
:   Gets a collection of objects that are based on the specified element names within a specified namespace.
[**hasAttributeNS**](/w/index.php?title=dom/methods/hasAttributeNS&action=edit&redlink=1)
:   Determines whether an attribute that has the specified namespace and name exists.
[**isDefaultNamespace**](/w/index.php?title=dom/methods/isDefaultNamespace&action=edit&redlink=1)
:   Indicates whether or not a namespace is the default namespace for a document.
[**isEqualNode**](/w/index.php?title=dom/methods/isEqualNode&action=edit&redlink=1)
:   Determines if two nodes are equal.
[**isSameNode**](/w/index.php?title=dom/methods/isSameNode&action=edit&redlink=1)
:   Determines if two node references refer to the same node.
[**isSupported**](/w/index.php?title=dom/methods/isSupported&action=edit&redlink=1)
:   Returns a value indicating whether or not the object supports a specific DOM standard.
[**load**](/w/index.php?title=apis/audio-video/methods/load&action=edit&redlink=1)
:   Resets the **IHTMLMediaElement** and loads a new media resource.
[**lookupNamespaceURI**](/w/index.php?title=dom/methods/lookupNamespaceURI&action=edit&redlink=1)
:   Gets the URI of the namespace associated with a namespace prefix, if any.
[**lookupPrefix**](/w/index.php?title=dom/methods/lookupPrefix&action=edit&redlink=1)
:   Gets the namespace prefix associated with a URI, if any.
**msClearEffects**
:   Clears all effects from the media pipeline.
**msInsertAudioEffect**
:   Inserts the specified audio effect into media pipeline.
[**msMatchesSelector**](/w/index.php?title=dom/methods/matchesSelector&action=edit&redlink=1)
:   Determines whether an object matches the specified selector.
**msSetMediaProtectionManager**
:   Specifies the media protection manager for a given media pipeline.
[**pause**](/w/index.php?title=apis/audio-video/methods/pause&action=edit&redlink=1)
:   Pauses the current playback and sets [**paused**](/w/index.php?title=apis/audio-video/properties/paused&action=edit&redlink=1) to TRUE.
[**play**](/w/index.php?title=apis/audio-video/methods/play&action=edit&redlink=1)
:   Loads and starts playback of a media resource.
[**removeAttributeNS**](/w/index.php?title=dom/methods/removeAttributeNS&action=edit&redlink=1)
:   Removes the specified attribute from the object.
[**setAttributeNodeNS**](/w/index.php?title=dom/methods/setAttributeNodeNS&action=edit&redlink=1)
:   Sets an [**attribute**](/w/index.php?title=dom/attributes&action=edit&redlink=1) object as part of the object.
[**setAttributeNS**](/w/index.php?title=dom/methods/setAttributeNS&action=edit&redlink=1)
:   Sets the value of the specified attribute within the specified namespace.

Â

#### Properties

The **media** object has these properties.

Property
:   Description
[**audioTracks**](/w/index.php?title=apis/audio-video/properties/audioTracks&action=edit&redlink=1)
:   Returns an [**AudioTrackList**](/apis/audio-video/AudioTrackList) object with the audio tracks for a given **video** element.
[**autobuffer**](/w/index.php?title=apis/audio-video/properties/autobuffer&action=edit&redlink=1)
:   The [**autobuffer**](/w/index.php?title=apis/audio-video/properties/autobuffer&action=edit&redlink=1) element is not supported by Internet ExplorerÂ 9. Use the [**preload**](/w/index.php?title=apis/audio-video/properties/preload&action=edit&redlink=1) element instead.

    This property is not supported for Metro style apps using JavaScript

[**autoplay**](/w/index.php?title=apis/audio-video/properties/autoplay&action=edit&redlink=1)
:   Gets or sets a value that indicates whether to start playing the media automatically.
[**buffered**](/w/index.php?title=apis/audio-video/properties/buffered&action=edit&redlink=1)
:   Gets a collection of buffered time ranges.
[**controls**](/w/index.php?title=apis/audio-video/properties/controls&action=edit&redlink=1)
:   Gets or sets a flag that indicates whether the client provides a set of controls for the media (in case the developer does not include controls for the player).
[**currentSrc**](/w/index.php?title=apis/audio-video/properties/currentSrc&action=edit&redlink=1)
:   Gets the address or URL of the current media resource (**video**,**audio**) that is selected by **IHTMLMediaElement**.
[**currentTime**](/w/index.php?title=apis/audio-video/properties/currentTime&action=edit&redlink=1)
:   Gets or sets the current playback position, in seconds.
[**defaultPlaybackRate**](/w/index.php?title=apis/audio-video/properties/defaultPlaybackRate&action=edit&redlink=1)
:   Gets or sets the default playback rate when the user is not using fast foward or reverse for a video or audio resource.
[**duration**](/w/index.php?title=apis/audio-video/properties/duration&action=edit&redlink=1)
:   Gets the duration, in seconds, of the current media resource, a `NaN` value if duration is not available, or `Infinity` if the media resource is streaming.
[**ended**](/w/index.php?title=apis/audio-video/properties/ended&action=edit&redlink=1)
:   Gets information about whether the playback has ended or not.
[**error**](/w/index.php?title=apis/audio-video/properties/error&action=edit&redlink=1)
:   Gets an **IHTMLMediaError** object representing the current error state of the media element.
[**initialTime**](/w/index.php?title=apis/audio-video/properties/initialTime&action=edit&redlink=1)
:   Gets the earliest possible position, in seconds, that the playback can begin.
[**localName**](/w/index.php?title=dom/properties/localName&action=edit&redlink=1)
:   Retrieves the local name of the fully qualified XML declaration for a node.
[**loop**](/w/index.php?title=apis/audio-video/properties/loop&action=edit&redlink=1)
:   Gets or sets a flag that specifies whether playback should restart after it completes.
**msAudioCategory**
:   Specifies the purpose of the audio or video media, such as background audio or alerts.
**msAudioDeviceType**
:   Specifies the output device id that the audio will be sent to.
**msPlayToDisabled**
:   Gets or sets whether the DLNA PlayTo device is available.
**msPlayToPrimary**
:   Gets or sets the primary DLNA PlayTo device.
**msPlayToSource**
:   Gets the source associated with the media element for use by the PlayToManager.
**msRealTime**
:   Specifies whether or not to enable low-latency playback on the media element.
[**muted**](/w/index.php?title=apis/audio-video/properties/muted&action=edit&redlink=1)
:   Gets or sets a flag that indicates whether the audio (either audio or the audio track on video media) is muted.
[**namespaceURI**](/w/index.php?title=dom/properties/namespaceURI&action=edit&redlink=1)
:   Retrieves the namespace URI of the fully qualified XML declaration for a node.
[**networkState**](/w/index.php?title=apis/audio-video/properties/networkState&action=edit&redlink=1)
:   Gets the current network activity for the element.
[**paused**](/w/index.php?title=apis/audio-video/properties/paused&action=edit&redlink=1)
:   Gets a flag that specifies whether playback is paused.
[**playbackRate**](/w/index.php?title=apis/audio-video/properties/playbackRate&action=edit&redlink=1)
:   Gets or sets the current speed for the media resource to play. This speed is expressed as a multiple of the normal speed of the media resource.
[**played**](/w/index.php?title=apis/audio-video/properties/played&action=edit&redlink=1)
:   Gets [**TimeRanges**](/w/index.php?title=apis/audio-video/HTMLTimeRanges&action=edit&redlink=1) for the current media resource that has been played.
[**prefix**](/w/index.php?title=dom/properties/prefix&action=edit&redlink=1)
:   Retrieves the local name of the fully qualified XML declaration for a node.
[**preload**](/w/index.php?title=apis/audio-video/properties/preload&action=edit&redlink=1)
:   Gets or sets a hint to how much buffering is advisable for a media resource, even if [**autoplay**](/w/index.php?title=apis/audio-video/properties/autoplay&action=edit&redlink=1) is not specified.
[**seekable**](/w/index.php?title=apis/audio-video/properties/seekable&action=edit&redlink=1)
:   Returns a [**TimeRanges**](/w/index.php?title=apis/audio-video/HTMLTimeRanges&action=edit&redlink=1) object that represents the ranges of the current media resource that can be seeked.
[**seeking**](/w/index.php?title=apis/audio-video/properties/seeking&action=edit&redlink=1)
:   Gets a flag that indicates whether the the client is currently moving to a new playback position in the media resource.
[**src**](/w/index.php?title=apis/audio-video/properties/src&action=edit&redlink=1)
:   The address or URL of the a media resource (**video**,Â **audio**) that is to be considered.
[**textContent**](/w/index.php?title=dom/properties/textContent&action=edit&redlink=1)
:   Sets or retrieves the text content of an object and any child objects.
[**volume**](/w/index.php?title=apis/audio-video/properties/volume&action=edit&redlink=1)
:   Gets or sets the volume level for audio portions of the media element.

Â

## See also

### Related pages (MSDN)

-   `Reference`
-   `audio`
-   `video`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

