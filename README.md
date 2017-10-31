# aframe-360-video-native-HLS-example

This is a basic example of 360 video playback, using A-Frame's latest master distribution build.

In this example, the 360 video is played using the `a-videosphere` primitive.
The video is rotated 180 degrees so the viewer appears to move forward.

The video element is specified with two possible sources. 
The first uses HLS format, for those browsers that support native HLS playback.
The second uses MP4 format, which is widely supported by available browsers.
(At present, this video file is not available in webm format.)
The browser implementation will automatically pick which source to use.

In some scenarios, particularly with mobile browsers, 
security rules will prevent the video from playing automatically.
To work around this limitation, window event handlers are attached that will try to start or toggle playback based on user input such as click.