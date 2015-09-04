---
title: TextTrack
tags:
  0: API
  1: Objects
  3: Audio
  4: Video
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'A media element can have a group of associated text tracks, known as the media element''s "list of text tracks".'
uri: apis/audio-video/TextTrack

---
# TextTracks

## Summary

A media element can have a group of associated text tracks, known as the media element's "list of text tracks".

## Properties

API Name
:   Summary
[activeCues](/apis/audio-video/TextTrack/activeCues)
:   Returns the text track cues from the text track list of cues that are currently active (i.e. that start before the current playback position and end after it), as a TextTrackCueList object.
[cues](/apis/audio-video/TextTrack/cues)
:   Returns the text track list of cues, as a TextTrackCueList object.
[inBandMetadataTrackDispatchType](/apis/audio-video/TextTrack/inBandMetadataTrackDispatchType)
:   Returns the text track in-band metadata track dispatch type string.

    This is a string extracted from the media resource specifically for in-band metadata tracks, to enable such tracks to be dispatched to different scripts in the document.

[kind](/apis/audio-video/TextTrack/kind)
:   Returns the text track kind string.
[label](/apis/audio-video/TextTrack/label)
:   Returns the text track label, if there is one, or the empty string otherwise (indicating that a custom label probably needs to be generated from the other attributes of the object if the object is exposed to the user).
[language](/apis/audio-video/TextTrack/language)
:   Returns the text track language string.
[mode](/apis/audio-video/TextTrack/mode)
:   The text track mode, represented by a string from the following list. "disabled": The text track disabled mode. "hidden": The text track hidden mode. "showing": The text track showing mode.

## Methods

API Name
:   Summary
[addCue](/apis/audio-video/TextTrack/addCue)
:   Adds the given cue to textTrack's text track list of cues.
[removeCue](/apis/audio-video/TextTrack/removeCue)
:   Removes the given cue from textTrack's text track list of cues.

## Events

*No events.*

## Notes

The track object contains the collection of [TextTrackCues](/apis/audio-video/TextTrackCue) (times and text) that are contained in the file that the **track** element represents.

#### WEBVTT

**TextTrackCues** within a **TextTrack** can be defined within a **[WebVTT](http://dev.w3.org/html5/webvtt/#dfnReturnLink-1)** file which is defined as an 8-bit Unicode Transformation Format (UTF-8) format text files that look like the following.

    WEBVTT

    00:00:01.878 --> 00:00:05.334
    Good day everyone, my name is John Smith

    00:00:08.608 --> 00:00:15.296
    This video will teach you how to
    build a sand castle on any beach

The file starts with the tag "WEBVTT" as the first line, followed by a line feed. The timing cues are in the format "HH:MM:SS.sss". The start and end time cues are separated by a space, two hyphens and a greater-than sign ( --\> ), and another space. The timing cues are on a line by themselves followed by a line feed. Immediately following the cue is the caption text. Text captions can be one or more lines. The only restriction is that there must be no blank lines between lines of text. The MIME type is "text/vtt".

## Related specifications

Specification
:   Status
[W3C HTML5 Specification](http://dev.w3.org/html5/spec/single-page.html)
:   W3C Editor's Draft

