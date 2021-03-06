# Docker container for MediaInfo
[![Docker Image Size](https://img.shields.io/microbadger/image-size/jlesage/mediainfo)](http://microbadger.com/#/images/jlesage/mediainfo) [![Build Status](https://drone.le-sage.com/api/badges/jlesage/docker-mediainfo/status.svg)](https://drone.le-sage.com/jlesage/docker-mediainfo) [![GitHub Release](https://img.shields.io/github/release/jlesage/docker-mediainfo.svg)](https://github.com/jlesage/docker-mediainfo/releases/latest) [![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://paypal.me/JocelynLeSage/0usd)

This is a Docker container for [MediaInfo](https://mediaarea.net/en/MediaInfo).

The GUI of the application is accessed through a modern web browser (no installation or configuration needed on the client side) or via any VNC client.

---

[![MediaInfo logo](https://images.weserv.nl/?url=raw.githubusercontent.com/jlesage/docker-templates/master/jlesage/images/mediainfo-icon.png&w=200)](https://mediaarea.net/en/MediaInfo)[![MediaInfo](https://dummyimage.com/400x110/ffffff/575757&text=MediaInfo)](https://mediaarea.net/en/MediaInfo)

MediaInfo is a convenient unified display of the most relevant technical and tag data for video and audio files.

---

## Quick Start

**NOTE**: The Docker command provided in this quick start is given as an example
and parameters should be adjusted to your need.

Launch the MediaInfo docker container with the following command:
```
docker run -d \
    --name=mediainfo \
    -p 5800:5800 \
    -v /docker/appdata/mediainfo:/config:rw \
    -v $HOME:/storage:ro \
    jlesage/mediainfo
```

Where:
  - `/docker/appdata/mediainfo`: This is where the application stores its configuration, log and any files needing persistency.
  - `$HOME`: This location contains files from your host that need to be accessible by the application.

Browse to `http://your-host-ip:5800` to access the MediaInfo GUI.
Files from the host appear under the `/storage` folder in the container.

## Documentation

Full documentation is available at https://github.com/jlesage/docker-mediainfo.

## Support or Contact

Having troubles with the container or have questions?  Please
[create a new issue].

For other great Dockerized applications, see https://jlesage.github.io/docker-apps.

[create a new issue]: https://github.com/jlesage/docker-mediainfo/issues
