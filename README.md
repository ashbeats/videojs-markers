Video.js Markers
===================
![Alt text](https://raw.github.com/spchuang/videojs-markers/master/screenshot.png "Screen shot of videojs.markers")

A plugin that displays customizable markers upon progress bars of the video with [Video.js](https://github.com/videojs/video.js/). This could be used to show video breaks and show overlaid text on the video when playback reaches the specific break point.

## Demo and Documentation
See [here](www.sampingchuang.com/videojs-markers)

JSBin Demo can be found [here] (http://jsbin.com/befob/7/edit)

## Feastures
* Display markers on progress bar, with hover-over tooltips
* Display break overlays
* Flexible styling
* Support dynamically adding and removing markers

## Quick Start
Add the 'videojs.markers.js' plugin and stylesheet after including videojs script and jQuery library

    <link href="http://vjs.zencdn.net/4.2/video-js.css" rel="stylesheet">
    <link href="videojs.markers.css" rel="stylesheet">
    <script src="http://code.jquery.com/jquery-2.0.3.min.js"></script>
    <script src="http://vjs.zencdn.net/4.2/video.js"></script>
    <script src='../src/videojs.markers.js'></script>

### Basic usage: display break markers in the video.
To add breaks in the video, simply add a new time (in seconds) in the list of breaks option. 
   
    // initialize video.js
    var video = videojs('test_video');

    //load the marker plugin
    video.markers({
      markers: [
         {time: 9.5, text: "this"},
         {time: 16,  text: "is"},
         {time: 23.6,text: "so"},
         {time: 28,  text: "cool"}
      ]
   });

### Customize marker style: 
The style of the markers could be modified by passing an optional setting "markerStyle" with your preference of css styles. 

    video.markers({
      setting: {
        markerStyle: {
          'width':'8px',
          'background-color': 'red'
        },
      },
      markers: [
         {time: 9.5, text: "this"},
         {time: 16,  text: "is"},
         {time: 23.6,text: "so"},
         {time: 28,  text: "cool"}
      ]    
    });
   
## History
- 0.4
   - change display_time to displayTime
   - markers now takes an array of object containing time, text, overlay text
   - add markerReached callback
   - markerTip and overlay text is now a clalback function for higher flexibility
   - Add many markers APIs for adding and removing markers dynamically.
- 0.1
   - initial release


## License
This project is licensed under MIT.
