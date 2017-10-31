# aframe-360-video-native-HLS-example

This is a basic example of 360 video playback, using [A-Frame's latest master](https://aframe.io/docs/master/introduction/#what-is-a-frame) distribution build.

In this example, the 360 video is played using the [`a-videosphere` primitive](https://aframe.io/docs/master/primitives/a-videosphere.html).
The video is rotated 180 degrees so the viewer appears to move forward.

[The video element is specified with two possible sources.](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/video#Multiple_sources_example)

The first uses [HLS](https://wikipedia.org/wiki/HTTP_Live_Streaming) format, for those browsers that support native HLS playback.

The second uses [MP4](https://wikipedia.org/wiki/MPEG-4_Part_14) format, which is widely supported by available browsers.
(At present, this video file is not available in webm format.)
The browser implementation will automatically pick which source to use.

In some scenarios, particularly with mobile browsers, 
security rules will prevent the video from playing automatically.
To work around this limitation, window event handlers are attached that will try to start or toggle playback based on user input such as click.