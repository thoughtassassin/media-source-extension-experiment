# media-source-extension-chatgpt

I started with ChatGPT but ChatGPT couldn't solve it. I used a solution that I saw work with webm files in Firefox. This solution wouldn't work with any other browser with webm:

https://github.com/joshuatz/mediasource-append-examples/blob/main/standard/index.js

I noticed that ChatGPT's script did work with fragmented mp4 files in Chrome. No other browser worked. So I tried the above script mentioned while formating mp4 files that are fragmented with GPAC's Mp4box with this command:

```MP4Box -dash 1000 -rap -frag-rap <your-file-here>```

This seems to work in all of the browsers I tested in so far (Firefox, Google and Safari in macOS Ventura 13.5.2).

To run the app:

<p><code>npm install</code><br />
<code>npm start</code></p>

To add more videos move mp4 files into the videos directory, run the command above and add the path to the outputed video file into the array of `vidClips` on line 35 in /views/index.html.