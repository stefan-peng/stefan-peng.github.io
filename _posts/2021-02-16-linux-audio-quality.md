---
title: Fixing Linux audio quality
header: Fixing Linux audio quality
description: Tweaks to PulseAudio and kernel parameters for better audio quality in Linux
permalink: /linux-audio-quality/
layout: post
---

On my Lenovo Thinkpad T460s, audio under Linux sometimes doesn't sound as good as under Windows. (There might have been a distro that didn't have this issue, but I can't remember which one.) Anyways, here are some tips I have found to improve audio quality in Linux.

## PulseAudio daemon configuration
From [this site](https://medium.com/@gamunu/enable-high-quality-audio-on-linux-6f16f3fe7e1f).
```
# $HOME/.config/pulse/daemon.conf

default-sample-format = float32le
default-sample-rate = 96000
alternate-sample-rate = 48000
default-sample-channels = 2
default-channel-map = front-left,front-right
default-fragments = 2
default-fragment-size-msec = 125
resample-method = soxr-vhq
#remixing-produce-lfe = no
#remixing-consume-lfe = no
high-priority = yes
nice-level = -11
realtime-scheduling = yes
realtime-priority = 9
rlimit-rtprio = 9
daemonize = no
```

## Linux kernel configuration
From the [Arch wiki](https://wiki.archlinux.org/index.php/Lenovo_ThinkPad_T460s).
```
# /etc/modprobe.d/modprobe.conf

options snd-hda-intel model=tpt460
```