---
title: Using XWayland in Sway
header: Using XWayland in Sway
permalink: /xwayland-sway/
layout: post
---

Ran into an issue earlier where I couldn't open an X app in Sway:

```
Gtk-WARNING **: 11:55:33.101: cannot open display: :0
```

Turns out I had set `GDK_BACKEND=wayland` in `.bashrc`, which caused issues with XWayland.

Solution: don't set `GDK_BACKEND=wayland` (as of 2021-03-26).
