---
title: Compressing mp4's
header: Compressing mp4's
description: Using ffmpeg to shrink h264 videos
permalink: /compress-videos-ffmpeg/
layout: post
---

Snippet from [this page](https://unix.stackexchange.com/questions/28803/how-can-i-reduce-a-videos-size-with-ffmpeg):

```
 ffmpeg -i input.mp4 -vcodec libx265 -crf 28 output.mp4
```

This uses `ffmpeg` to re-encode an h264 video with the h265 codec with a Constant Rate Factor of 28 (lower number = higher bitrate).
