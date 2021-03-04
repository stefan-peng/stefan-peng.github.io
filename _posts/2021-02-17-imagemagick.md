---
title: Converting images with Imagemagick
header: Converting images with Imagemagick
permalink: /imagemagick/
layout: post
---

I recently needed to convert a bunch of TIFF files to PNGs. I knew ImageMagick could do it, but couldn't remember how. As it turns out, it is very straightforward:

```
convert input.tiff output.png
```

To convert multiple files, I ran `convert` in a loop:
```
for i in *.tiff; do convert $i $i.png; done
```

I'm sure there is some shell magic that can deal with the extensions correctly, but I just used `rename` to fix them:

```
rename .tiff.png .png *.tiff.png
rm *.tiff
```

**Update 2/17/2021**

Here's a better way to do it:
```
for i in *.tiff; do convert $i "${i%.*}".png; done
```

The key part, `"${i%.*}"`, expands to the filename without the file extension.
