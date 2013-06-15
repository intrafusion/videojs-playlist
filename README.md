Video.js playlist
===================
A video-js plugin to play multiple audio tracks or multiple videos.

*Rationale:* The main goal in developing this plugin is play **audio** files. Playing audio is possible either by swapping the ```<video>``` for an ```<audio>``` tag or by simply feeding audio tracks to the ```<video>``` tag. Both approaches have their pluses and minuses which are [documented here in the video.js issues.](https://github.com/videojs/video.js/issues/537?source=cc)

Using the Plugin
----------------
The plugin automatically registers itself when you include video.playlist.js in your page:

    <script src='videojs.playlist.js'></script>

You probably want to include the default stylesheet, too. It provides some basic styling to indicate what the currentTrack is:

    <link href="videojs.playlist.css" rel="stylesheet">

The Playlist plugin currently takes two options:

    myPlayerPlaylist.playlist({
      'tracksClassName': 'trackSelector', 
      'continuous': true
    });
    
```tracksClassName``` is a required option. It is a string of the className **without** the beginning ```.```. The tracksClassName element **must** possess  ```data-src="/path/to/track.m4a"``` and ```data-index="3"``` attributes needed for switching tracks. See the HTML in example.html for explanation.

```continuous``` is optional. It specifies whether the playlist should play the next track after the previous one finishes. Setting this to ```false``` prevents the continuous playback. Not including this option is the same as setting it to ```true```.

Future options being considered include: 1) a shuffle button to shuffle tracks and 2) rendering the playlist using JS such that all one needs is JSON to build the playlist.


