TOPICS: <audio>
AUTHORS: Eric Shepherd; eshepherd@mozilla.com; github:a2sheppy
         Mojtaba Javan; javan.mojtaba@gmail.com; github:mrmowji
         Masahiro Fujimoto; mfujimot@gmail.com; github:mfuji09
         Jen Simmons; jensimmons@github.com; github:jensimmons
         Joe Medley; jmedley@chromium.org; github:jpmedley
         Connor Shea; connor.james.shea@gmail.com; github:connorshea
         Taylor Hunt; tigt@github.com; github:tigt
         Chris Mills; chrisdavidmills@mozilla.net; mdn:chrisdavidmills
         Sphinx; SphinxKnight@github.com; github:SphinxKnight
         Stephan Max; stephanmax@mozilla.net; mdn:stephanmax
         Roy Vanegas; code-warrior@github.com; github:code-warrior
         Eric Bailey; ericwbailey@github.com; github:ericwbailey
         Karl Groves; karlgroves@gmail.com; github:karlgroves
         Christian Weiske; cweiske@github.com; github:cweiske
         Teoli; teoli@mozilla.net; mdn:teoli
         Michael[tm] Smith; mike@w3.org; github:sideshowbarker
         Druzion; Druzion@mozilla.net; mdn:Druzion
         Sebastian Zartner; SebastianZ@github.com; github:SebastianZ
         Jérémie Patonnier; Jeremie@mozilla.net; mdn:Jeremie
         Rob Wu; rob@robwu.nl; github:Rob--W
         Tom Morris; tommorris@mozilla.net; mdn:tommorris
         Karen Scarfone; kscarfone@mozilla.net; mdn:kscarfone
         Keiichi; ethertank@mozilla.net; mdn:ethertank
         Janet Swisher; jmswisher@github.com; github:jmswisher
         Nickolay Ponomarev; asqueella@gmail.com; github:nickolay
         Mateus Machado Luna; mateus.m.luna@mozilla.net; mdn:mateus.m.luna
         Thierry Régagnon; tregagnon@github.com; github:tregagnon
         Florian Scholz; fscholz@mozilla.net; mdn:fscholz
         Christian Sonne; cers@mozilla.net; mdn:cers
         Jonathan Wilsson; jwilsson@github.com; github:jwilsson

# `<audio>`

The **HTML `<audio>` element** is used to embed sound content in documents. It may contain one or
more audio sources, represented using the `src` attribute or the [`<source>`](/en/webfrontend/<source>)
element: the browser will choose the most suitable one. It can also be the destination for streamed
media, using a `MediaStream`.

The above example shows simple usage of the `<audio>` element. In a similar manner
to the [`<img>`](/en/webfrontend/<img>) element, we include a path to the media we want to embed
inside the `src` attribute; we can include other attributes to specify information such as whether
we want it to autoplay and loop, whether we want to show the browser's default audio controls, etc.

The content inside the opening and closing `<audio></audio>` TOPICS is shown as a
fallback in browsers that don't support the element.

Browsers don't all support the same audio formats; you can provide multiple sources inside
nested [`<source>`](/en/webfrontend/<source>) elements, and the browser will then use the first one
it understands:

```html
<audio controls>
  <source src="myAudio.mp3" type="audio/mpeg">
  <source src="myAudio.ogg" type="audio/ogg">
  <p>Your browser doesn't support HTML5 audio. Here is
     a <a href="myAudio.mp4">link to the audio</a> instead.</p>
</audio>
```

Other Usage Notes:

- If you don't specify the `controls` attribute, the audio player won't include the browser's
default `controls`; you can create your own custom `controls`
using JavaScript and the `HTMLMediaElement` API.
- To allow precise control over your audio content, `HTMLMediaElement`s fire many different `events`.
- You can also use the Web Audio API to directly generate and
manipulate audio streams from JavaScript code.
- `<audio>` elements can't have subtitles/captions associated with them in the same way that
[`<video>`](/en/webfrontend/<video>) elements can. See WebVTT and Audio
by Ian Devlin for some useful information and workarounds.

A good general source of information on using HTML `<audio>` is
the Video and audio content beginner's tutorial.

## Attributes

This element's attributes include the [global attributes](https://wiki.developer.mozilla.org/en-US/docs/HTML/Global_attributes).

| Attribute | Description |
| :-- | :-- |
| `autoplay` | A Boolean attribute: if specified, the audio will automatically begin playback as soon as it can do so, without waiting for the entire audio file to finish downloading.<br>**Note:** Sites that automatically play audio (or videos with an audio track) can be an unpleasant<br>experience for users, so should be avoided when possible. If you must offer autoplay functionality,<br>you should make it opt-in (requiring a user to specifically enable it). However, this can be useful<br>when creating media elements whose source will be set at a later time, under user control.
| `controls` | If this attribute is present, the browser will offer controls to allow the user to control audio playback, including volume, seeking, and pause/resume playback.
| `crossorigin` | This enumerated attribute indicates whether to use CORS to fetch the related image. CORS-enabled resources can be reused in the `<canvas>` element without being tainted. The allowed values are:
| `anonymous` | Sends a cross-origin request without a credential. In other words, it sends the `Origin:` HTTP header without a cookie, X.509 certificate, or performing HTTP Basic authentication. If the server does not give credentials to the origin site (by not setting the `Access-Control-Allow-Origin:` HTTP header), the image will be tainted, and its usage restricted.
| `use-credentials` |Sends a cross-origin request with a credential. In other words, it sends the `Origin:` HTTP header with a cookie, a certificate, or performing HTTP Basic authentication. If the server does not give credentials to the origin site (through `Access-Control-Allow-Credentials:` HTTP header), the image will be tainted and its usage restricted.<br>When not present, the resource is fetched without a CORS request (i.e. without sending the `Origin:` HTTP header), preventing its non-tainted used in [`<canvas>`](/en/webfrontend/<canvas>) elements. If invalid, it is handled as if the enumerated keyword **anonymous** was used. See CORS settings attributes for additional information. |
| `currentTime` | Reading `currentTime` returns a double-precision floating-point value indicating the current playback position, in seconds, of the audio. If the audio's metadata isn't available yet—thereby preventing you from knowing the media's start time or duration—`currentTime` instead indicates, and can be used to change, the time at which playback will begin. Otherwise, setting `currentTime` sets the current playback position to the given time and seeks the media to that position if the media is currently loaded.<br>If the audio is being streamed, it's possible that the user agent may not be able to obtain some parts of the resource if that data has expired from the media buffer. Other audio may have a media timeline that doesn't start at 0 seconds, so setting `currentTime` to a time before that would fail. For example, if the audio's media timeline starts at 12 hours, setting `currentTime` to 3600 would be an attempt to set the current playback position well before the beginning of the media, and would fail. The `getStartDate()` method can be used to determine the beginning point of the media timeline's reference frame. |
| `disableRemotePlayback` | A Boolean attribute used to disable the capability of remote playback in devices that are attached using wired (HDMI, DVI, etc.) and wireless technologies (Miracast, Chromecast, DLNA, AirPlay, etc). See this proposed specification for more information.<br>**Note:** In Safari, you can use `x-webkit-airplay="deny"` as a fallback.
| `duration` | A double-precision floating-point value which indicates the duration (total length) of the audio in seconds, on the media's timeline. If no media is present on the element, or the media is not valid, the returned value is `NaN`. If the media has no known end (such as for live streams of unknown duration, web radio, media incoming from WebRTC, and so forth), this value is `+Infinity`.
| `loop` | A Boolean attribute: if specified, the audio player will automatically seek back to the start upon reaching the end of the audio.
| `muted` | A Boolean attribute that indicates whether the audio will be initially silenced. Its default value is `false`. |
| `preload` | This enumerated attribute is intended to provide a hint to the browser about what the author thinks will lead to the best user experience. It may have one of the following values:<br>`none`: Indicates that the audio should not be preloaded.<br>`metadata`: Indicates that only audio metadata (e.g. length) is fetched.<br>`auto`: Indicates that the whole audio file can be downloaded, even if the user is not expected to use it.<br>empty string: A synonym of the `auto` value.<br><br>The default value is different for each browser. The spec advises it to be set to `metadata`<br>**Notes:** The autoplay attribute has precedence over preload. If autoplay is specified, the browser<br>would obviously need to start downloading the audio for playback.<br>The browser is not forced by the specification to follow the value of this attribute; it is a mere hint.
| `src` | The URL of the audio to embed. This is subject to HTTP access controls. This is optional; you may instead use the [`<source>`](/en/webfrontend/<source>) element within the audio block to specify the audio to embed.

## Events

| Event Name | Fired When |
| :-- | :-- |
| `audioprocess` | The input buffer of a `ScriptProcessorNode` is ready to be processed.
| `canplay` | The browser can play the media, but estimates that not enough data has been loaded to play the media up to its end without having to stop for further buffering of content.
| `canplaythrough` | The browser estimates it can play the media up to its end without stopping for content buffering.
| `complete` | The rendering of an `OfflineAudioContext` is terminated.
| `durationchange` | The `duration` attribute has been updated.
| `emptied` | The media has become empty; for example, this event is sent if the media has already been loaded (or partially loaded), and the `load()` method is called to reload it.
| `ended` | Playback has stopped because the end of the media was reached.
| `loadeddata` | The first frame of the media has finished loading.
| `loadedmetadata` | The metadata has been loaded.
| `pause` | Playback has been paused.
| `play` | Playback has begun.
| `playing` | Playback is ready to start after having been paused or delayed due to lack of data.
| `ratechange` | The playback rate has changed.
| `seeked` | A seek operation completed.
| `seeking` | A seek operation began.
| `stalled` | The user agent is trying to fetch media data, but data is unexpectedly not forthcoming.
| `suspend` | Media data loading has been suspended.
| `timeupdate` | The time indicated by the `currentTime` attribute has been updated.
| `volumechange` | The volume has changed.
| `waiting` | Playback has stopped because of a temporary lack of data

## Usage Notes

Browsers don't all support the same audio formats; you can provide multiple sources inside
nested [`<source>`](/en/webfrontend/<source>) elements, and the browser will then use the
first one it understands:

We offer a substantive and thorough guide to media file types and the audio codecs that can be used
within them. Also available is a guide to the codecs supported for video.

Other Usage Notes:

- If you don't specify the `controls` attribute, the audio player won't include the browser's
default controls.
You can, however, create your own custom controls using JavaScript and the `HTMLMediaElement` API.
- To allow precise control over your audio content, `HTMLMediaElements` fire many different events.
This also provides a way to monitor the audio's fetching process so you can watch for errors or
detect when enough is available to begin to play or manipulate it.
- You can also use the Web Audio API to directly generate and manipulate audio streams from JavaScript
code rather than streaming pre-existing audio files.
- `<audio>` elements can't have subtitles or captions associated with them in the same way that
[`<video>`](/en/webfrontend/<video>) elements can. See [WebVTT and Audio](https://www.iandevlin.com/blog/2015/12/html5/webvtt-and-audio)
by Ian Devlin for some useful information and workarounds.

A good general source of information on using HTML
`<audio>` is the Video and audio content beginner's tutorial.

### Styling with CSS

The `<audio>` element has no intrinsic visual output of its own unless the `controls` attribute is
specified, in which case the browser's default controls are shown.

The default controls have a `display` value of `inline` by default, and it is often a good
idea set the value to `block` to improve control over positioning and layout,
unless you want it to sit within a text block or similar.

You can style the default controls with properties that affect the block as a single unit,
so for example you can give it a `border` and `border-radius`, `padding`, `margin`, etc.
You can't however style the individual components inside the audio player (e.g. change the button
size or icons, change the font, etc.), and the controls are different across the different browsers.

To get a consistent look and feel across browsers, you'll need to create custom controls; these can
be marked up and styled in whatever way you want, and then JavaScript can be used along with the
`HTMLMediaElement` API to wire up their functionality.

Video player styling basics provides some useful styling techniques — it is written in the
context of [`<video>`](/en/webfrontend/<video>), but much of it is equally applicable to `<audio>`.

### Detecting addition and removal of tracks

You can detect when tracks are added to and removed from an `<audio>` element using the
`addtrack` and `removetrack` events. However, these events aren't sent directly to
the `<audio>` element itself. Instead, they're sent to the track list object within the `<audio>`
element's `HTMLMediaElement` that corresponds to the type of track that was added to the element:

`HTMLMediaElement.audioTracks`

An `AudioTrackList` containing all of the media element's audio tracks. You can add a
listener for `addtrack` to this object to be alerted when new audio tracks are added to the element.

`HTMLMediaElement.videoTracks`

Add an `addtrack` listener to this `VideoTrackList` object to be informed when
video tracks are added to the element.

`HTMLElement.textTracks`

Add an `addtrack` event listener to this `TextTrackList` to be notified when new
text tracks are added to the element.

!!! warn "Don't try this at home"
    Note: Even though it's an `<audio>` element, it still has video and text track lists, and can in
    fact be used to present video, although the use interface implications can be odd.

For example, to detect when audio tracks are added to or removed from an `<audio>` element,
you can use code like this:

```javascript
var elem = document.querySelector("audio");

elem.audioTrackList.onaddtrack = function(event) {
  trackEditor.addTrack(event.track);
};

elem.audioTrackList.onremovetrack = function(event) {
  trackEditor.removeTrack(event.track);
};
```

This code watches for audio tracks to be added to and removed from the element, and calls a
hypothetical function on a track editor to register and remove the track from the editor's
list of available tracks.

You can also use `addEventListener()` to listen for the
`addtrack` and `removetrack` events.

## Examples

### Basic Usage

The following example shows simple usage of the `<audio>` element to play an OGG file. It will
autoplay due to the `autoplay` attribute, and also includes fallback content.

```html
<!-- Simple audio playback -->
<audio
  src="AudioTest.ogg"
  autoplay>
  Your browser does not support the <code>audio</code> element.
</audio>
```

### `<audio>` element with `<source>` element

This example specifies which audio track to embed using the `src` attribute on a nested
[`<source>`](/en/webfrontend/<source>) element rather than directly on the `<audio>` element. It is
always useful to include the file's MIME type inside the `type` attribute, as the browser is able to
instantly tell if it can play that file, and not waste time on it if not.

```html
<audio controls="controls">
  <source src="foo.wav" type="audio/wav">
  Your browser does not support the <code>audio</code> element.
</audio>
```

### `<audio>` with multiple `<source>` elements

This example includes multiple [`<source>`](/en/webfrontend/<source>) elements. The browser tries to
load the first source element (Opus) if it is able to play it; if not it falls back to the second
(Vorbis) and finally back to MP3:

```html
<audio controls="">
 <source src="foo.opus" type="audio/ogg; codecs=opus"/>
 <source src="foo.ogg" type="audio/ogg; codecs=vorbis"/>
 <source src="foo.mp3" type="audio/mpeg"/>
</audio>
```

## Accessibility Concerns

Audio with spoken dialog should provide both captions and transcripts that accurately describe its
content. Captions, which are specified using WebVTT, allow people who are experiencing hearing loss
to understand an audio recording's content as the recording is being played, while transcripts allow
people who need additional time to be able to review the recording's content at a pace and format
that is comfortable for them.

If automatic captioning services are used, it is important to review the generated content to ensure
it accurately represents the source audio.

The `<audio>` element doesn't directly support WebVTT. You will have to find a library or framework
that provides the capability for you, or write the code to display captions yourself.

In addition to spoken dialog, subtitles and transcripts should also identify music and sound effects
that communicate important information. This includes emotion and tone. For example, in the WebVTT
below, note the use of square brackets to provide tone and emotional insight to the viewer;
this can help establish the mood otherwise provided using music, nonverbal sounds and crucial
sound effects, and so forth.

```http
1
00:00:00 --> 00:00:45
Energetic techno music]

2
00:00:46 --> 00:00:51
Welcome to the Time Keeper's podcast! In this episode we're discussing which Swisswatch is a wrist switchwatch?

16
00:00:52 --> 00:01:02
Laughing] Sorry! I mean, which wristwatch is a Swiss wristwatch?
```

Also it's a good practice to provide some content (such as the direct download link) as a fallback
for viewers who use a browser in which the `<audio>` element is not supported:

```html
<audio controls>
  <source src="myAudio.mp3" type="audio/mpeg">
  <source src="myAudio.ogg" type="audio/ogg">
  <p>
    Your browser doesn't support HTML5 audio.
    Here is a <a href="myAudio.mp4">link to download the audio</a> instead.
  </p>
</audio>
```

- [MDN Subtitles and closed caption — Plugins](https://wiki.developer.mozilla.org/en-US/docs/Plugins/Flash_to_HTML5/Video/Subtitles_captions)
- [Web Video Text Tracks Format (WebVTT)](https://wiki.developer.mozilla.org/en-US/docs/Web/API/WebVTT_API)
- [WebAIM: Captions, Transcripts, and Audio Descriptions](https://webaim.org/techniques/captions/)
- [MDN Understanding WCAG, Guideline 1.2 explanations](https://wiki.developer.mozilla.org/en-US/docs/Web/Accessibility/Understanding_WCAG/Perceivable#Guideline_1.2_%E2%80%94_Providing_text_alternatives_for_time-based_media)
- [Understanding Success Criterion 1.2.1 | W3C Understanding WCAG 2.0](https://www.w3.org/TR/UNDERSTANDING-WCAG20/media-equiv-av-only-alt.html)
- [Understanding Success Criterion 1.2.2 | W3C Understanding WCAG 2.0](https://www.w3.org/TR/UNDERSTANDING-WCAG20/media-equiv-captions.html)

## Technical Summary

|  |  |
| :-- | :-- |
| **Content categories** | Flow content, phrasing content, embedded content. If it has a controls attribute: interactive content and palpable content.|
| **Permitted content** | If the element has a `src` attribute: zero or more [`<track>`](/en/webfrontend/<track>) elements followed by transparent content that contains no `<audio>` or [`<video>`](/en/webfrontend/<video>) media elements.<br>Else: zero or more [`<source>`](/en/webfrontend/<source>) elements followed by zero or more [`<track>`](/en/webfrontend/<track>) elements followed by transparent content that contains no `<audio>` or [`<video>`](/en/webfrontend/<video>) media elements.|
| **Tag omission** | None, both the starting and ending tag are mandatory.|
| **Permitted parents** | Any element that accepts embedded content.|
| **Permitted ARIA roles** | [`application`](https://w3c.github.io/aria/#application) |
| **DOM interface** | `HTMLAudioElement`|
