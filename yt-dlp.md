# Download Youtube video or audio

[yt-dlp github](https://github.com/yt-dlp/yt-dlp)

## Setup in windows

* Download and setup yt-dlp
* Download and setup ffmpeg

## How to download only audio from youtube video?

```cmd
SET VIDEO_URL=https://www.youtube.com/watch?v=7t20Nrcs7eo

yt-dlp -o "katha-upanishad-01.mp3" --extract-audio --audio-format mp3 --ffmpeg-location E:\apps\ffmpeg %VIDEO_URL%
```

## Download enire playlist videos and convert to audio - Windows

```cmd
SET PLAYLIST_URL=https://www.youtube.com/playlist?list=PL9GuvNbBtuEg34ZTw1bV7a0WcFLbrpwXx

yt-dlp -o "%(playlist)s/%(playlist_index)s-%(title)s.%(ext)s"  --extract-audio --audio-format mp3 --ffmpeg-location E:\apps\ffmpeg %PLAYLIST_URL%
```
