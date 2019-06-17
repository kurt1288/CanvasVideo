# CanvasVideo
A simple way to convert an HTML canvas to a webm video format

CanvasVideo.js is a basic implementation of the [MediaStream Recording API](https://developer.mozilla.org/en-US/docs/Web/API/MediaStream_Recording_API).

### Browser compatibility
* Chrome
* Firefox

### Installing
Download CanvasVideo.js and add it with the normal script tag:

    <script src="canvasvideo.js"></script>

or you can import it if you are using modules:

    import { CanvasVideo } from "canvasvideo.js"
    
### Usage
First you must create a new video:

    const video = new CanvasVideo(canvas[, framerate, bitrate]);

Parameters:

**canvas**: This is the canvas DOM element you wish to record from.

**framerate** (OPTIONAL): The rate of capture of each frame. Default is 30.

**bitrate** (OPTIONAL): The bitrate of the capture video, in bits. Default is 2500000 (2.5 Mbps).

### Methods

After you have create the video, you can begin capture with:

    video.Start();
    
When recording is complete:

    video.Stop();
    
When you wish to save the video:

    video.Save([filename]);
    
A filename is optional. If no filename is specified, "*canvasvideo.webm*" will be used.

## License

Released under the MIT License.
