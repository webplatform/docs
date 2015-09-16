---
title: 'addCue'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/audio-video/TextTrack
    href: /apis/audio-video/TextTrack
  return_type:
    predicate: 'Returns an object of type  '
    value: ''
    href: /apis/audio-video/TextTrack
standardization_status: 'W3C Editor''s Draft'
summary: 'Adds the given cue to textTrack''s text track list of cues.'
tags:
  0: API
  1: Object
  2: Methods
  4: Audio
  5: Video
uri: apis/audio-video/TextTrack/addCue

---
## Summary

Adds the given cue to textTrack's text track list of cues.

Method of [apis/audio-video/TextTrack](/apis/audio-video/TextTrack)[apis/audio-video/TextTrack](/apis/audio-video/TextTrack)

## Syntax

``` js
var  = TextTrack.addCue(cue);
```

## Parameters

### cue

 Data-type
:   String

 "cue" is of type TextTrackCue.

## Return Value

Returns an object of type

## Examples

using addCue in javascript and setting several properties:

``` js
myTextTrack = myPlayer.addTextTrack( 'subtitles','myLabel','en' );
var cue0 = new TextTrackCue(516.517,531.532, 'it had become much easier after the so called united resistance movement');
cue0.id = 'cue0';
cue0.pauseOnExit = false;
myTextTrack.addCue(cue0);

myTextTrack.mode = "showing";
```

This addCue does NOT work, but should. Several things go wrong. First of all, it does not recognize the percent sign. Secondly, the cue text is an html symbol, which is not interpreted as html.

``` js
var cue1 = new TextTrackCue(3.300,13.130, '&8594;');
cue1.id = 'cue1';
myTextTrack.addCue(cue1);
cue1.line = '50%';
cue1.position = '25%';
```

## Related specifications

[W3C HTML5 Specification](http://dev.w3.org/html5/spec/single-page.html)
:   W3C Editor's Draft
