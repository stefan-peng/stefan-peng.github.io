---
title: Removing GRUB from MBR
header: Removing GRUB from MBR
description: 
permalink: /remove-grub-mbr/
layout: post
---

This is becoming less relevant as news systems all have UEFI, but if you want to remove GRUB from a system with BIOS, here's how to do it.

1. Boot into Windows or Windows recovery disk
2. Assuming disk with GRUB is `C:\`, run the following from an elevated command prompt: 
    ```
    bootsect /nt60 C: /mbr
    ```
    This will update the Master Boot Record of the drive without affecting the partition table. 