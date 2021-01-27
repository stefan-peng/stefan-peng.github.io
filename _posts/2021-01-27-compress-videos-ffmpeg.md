---
title: Compress mp4 Videos Using ffmpeg
header: Compress mp4 Videos Using ffmpeg
description: Using ffmpeg to re-encode h264 videos to save space
permalink: /compress-videos-ffmpeg/
layout: post
---

Snippet from [this page](https://unix.stackexchange.com/questions/28803/how-can-i-reduce-a-videos-size-with-ffmpeg):

```
 ffmpeg -i input.mp4 -vcodec libx265 -crf 28 output.mp4
```

This uses `ffmpeg` to re-encode an h264 video with the h265 codec with a Constant Rate Factor of 28 (lower number = higher bitrate).