---
title: Importing Spotify GPG key on Arch
header: Importing Spotify GPG key on Arch
permalink: /spotify-gpg-arch/
layout: post
---

If you are trying to install Spotify on Arch, you might see this:

```
:: Importing keys with gpg...
gpg: keyserver receive failed: Server indicated a failure
problem importing keys
```

Manually importing the GPG key from Spotify's repo seems to fix the problem:
```
curl -sS https://download.spotify.com/debian/pubkey_0D811D58.gpg | gpg --import -
```

If necessary, update the key URL from the Debian/Ubuntu instructions given [here](https://www.spotify.com/us/download/linux/).
