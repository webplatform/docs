---
title: 'MediaStream Recording'
notes:
  - 'This article is currently being worked on. (Author? Date?)'
readiness: 'In Progress'
standardization_status: 'W3C Working Draft'
summary: 'Allows users to record camera/microphone''s streams'
tags:
  - API_Listings
  - API
  - Media_Recorder
uri: 'apis/media recorder'

---
## Summary

Allows users to record camera/microphone's streams

[MediaRecorder](/apis/media_recorder/MediaRecorder)
:

## Usage

     This API attempts to make basic recording very simple, while still allowing for more complex use cases. In the simplest case, the application instantiates the MediaRecorder object, calls record() and then calls stopRecord() or waits for the MediaStream to be ended. The contents of the recording will be made available in the platform's default encoding via the dataavailable event. Functions are available to query the platform's available set of encodings, and to select the desired ones if the author wishes. The application can also choose how much data it wants to receive at one time. By default a Blob containing the entire recording is returned when the recording finishes. However the application can choose to receive smaller buffers of data at regular intervals.

## See also

### External resources

-   [MediaStream Recording](http://www.w3.org/TR/mediastream-recording/)
-   [MediaStream Recording - W3C Working Draft 05 February 2013](http://www.w3.org/TR/2013/WD-mediastream-recording-20130205/)
-   [Device APIs working group](http://www.w3.org/2009/dap/)
-   [Media Capture Wiki](http://www.w3.org/wiki/Media_Capture)
