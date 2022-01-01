<p align="center">
<img height="256" src="https://github.com/iina/iina/raw/master/iina/Assets.xcassets/AppIcon.appiconset/iina-icon-256.png" />
</p>

<h1 align="center">IINA+</h1>

<p align="center">IINA+ is a special build of the <b>modern</b> video player <a href="https://github.com/iina/iina">IINA</a> with additional features and bugfixes.</p>

---

## Features

* HDR playback

## Planed features

* Danmaku

## About youtube-dl

We no longer embed the outdated youtube-dl. Users must install `yt-dlp` manually for playing network resources.

```sh
$ brew install yt-dlp
```

## Build

```bash
$ cp other/*-iina.rb $(brew --repo homebrew/core)/Formula # Copy custom mpv and ffmpeg formula into homebrew repo
$ make depends # Build dependencies
$ make build # Build iina itself
```
  - Tips:
    - Change URL in the shell script if you want to download arch-specific binaries. By default, it will download the universal ones. You can download other binaries from `https://iina.io/dylibs/${ARCH}/fileList.txt` where `ARCH` can be `universal`, `arm64` and `x86_64`.
    - If you want to build an older IINA version, make sure to download the correponding dylibs. For example, `https://iina.io/dylibs/1.2.0/universal/fileList.txt`.

## Binaries

* Intel (x64): Download artifacts in <https://github.com/iina-plus/iina/actions>
* Apple M1 (aarch64): Download assets in <https://github.com/iina-plus/iina/releases>
