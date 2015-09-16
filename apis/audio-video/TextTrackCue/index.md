---
title: 'TextTrackCue'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'A text track cue is the unit of time-sensitive data in a text track corresponding, for instance, for subtitles and captions to the text that appear at a particular time and disappear at another time.'
tags:
  0: API
  1: Objects
  3: Audio
  4: Video
uri: apis/audio-video/TextTrackCue

---
## Summary

A text track cue is the unit of time-sensitive data in a text track corresponding, for instance, for subtitles and captions to the text that appear at a particular time and disappear at another time.

## Properties

API Name
:   Summary

[align](/apis/audio-video/TextTrackCue/align)
:   A string representing the text track cue alignment, as follows. If it is start alignment: the string "start". If it is middle alignment: the string "middle". If it is end alignment: the string "end". If it is left alignment: the string "left". If it is right alignment: the string "right". Default is "middle".

[endTime](/apis/audio-video/TextTrackCue/endTime)
:   The text track cue end time, in seconds.

[id](/apis/audio-video/TextTrackCue/id)
:   Gets or sets a text track cue identifier.

[line](/apis/audio-video/TextTrackCue/line)
:   The text track cue line position. In the case of the value being auto, the string "auto" is returned.

[pauseOnExit](/apis/audio-video/TextTrackCue/pauseOnExit)
:   Returns the pause-on-exit flag on a TextTrackCue. When the flag is true, playback will pause when it reaches the cue's endTime.

[position](/apis/audio-video/TextTrackCue/position)
:   The text track cue text position.

[size](/apis/audio-video/TextTrackCue/size)
:   The text track cue size.

[snapToLines](/apis/audio-video/TextTrackCue/snapToLines)
:   Returns the text track cue snap-to-lines flag setting.

[startTime](/apis/audio-video/TextTrackCue/startTime)
:   The text track cue start time, in seconds.

[text](/apis/audio-video/TextTrackCue/text)
:   The text track cue text in raw, unparsed form.

[track](/apis/audio-video/TextTrackCue/track)
:   Returns the TextTrack object to which this text track cue belongs, if any, or null otherwise.

[vertical](/apis/audio-video/TextTrackCue/vertical)
:   A string representing the text track cue writing direction, as follows. If it is horizontal: The empty string. If it is vertical growing left: The string "rl". If it is vertical growing right: The string "lr".

## Methods

API Name
:   Summary

[getCueAsHTML](/apis/audio-video/TextTrackCue/getCueAsHTML)
:   Returns the text track cue text as a DocumentFragment of HTML elements and other DOM nodes.

## Events

*No events.*

## Notes

Individual cues are returned from a [TextTrackCueList](/apis/audio-video/TextTrackCueList) object (collection of cues). Cues can also be created and added to a track.

## Related specifications

[W3C HTML5 Specification](http://dev.w3.org/html5/spec/single-page.html)
:   W3C Editor's Draft
