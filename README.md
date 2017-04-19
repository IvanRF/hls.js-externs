# hls.js-externs
[hls.js](https://github.com/video-dev/hls.js) externs for use with [Closure Compiler](https://developers.google.com/closure/compiler/).

**Based on [hls.js v0.7.5](https://github.com/video-dev/hls.js/releases/tag/v0.7.5).**

----------
## Example ##
    
Before minification:

    if (Hls.isSupported()) {
    	var video = document.getElementById("video");
    	var src = video.dataset.source;
    	var hls = new Hls();
    	hls.loadSource(src);
    	hls.attachMedia(video);
    	hls.on(Hls.Events.MANIFEST_PARSED, function() {
    		video.play();
    	});
    }

After minification:

    if(Hls.isSupported()){var a=document.getElementById("video"),b=a.dataset.source,c=new Hls;c.loadSource(b);c.attachMedia(a);c.on(Hls.Events.MANIFEST_PARSED,function(){a.play()});