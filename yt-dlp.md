# Download Youtube video or audio

If I have a computer (Laptop/Desktop), and broadband internet connection

* How do I download video so that I can listen and watch offline?
* How do I convert video to audio so that I can listen?

Why?

* **I might repeatedly learn/listen. so it is better to download and keep it offline**

## Setup in windows

* Download and setup **yt-dlp** program
  * Go to [yt-dlp home page](https://github.com/yt-dlp/yt-dlp?#Installation)
  * Click **Windows X64**. This downloads a file **yt-dlp.exe** to **Downloads** folder
  * Create a directory: `mkdir C:\apps\bin`
  * Copy **yt-dlp.exe** - `copy %USERPROFILE%\Downloads\yt-dlp.exe C:\apps\bin`
  * Add `C:\apps\bin` directory to the **PATH** environment variables for your account

## How to download video?

The below videos are from **karate kid** movie. Download and watch

```cmd
SET VIDEO_URL=https://www.youtube.com/watch?v=8INjmc-WWSY

yt-dlp -o "01-karate-kid-jacket-on-off.%(ext)s" %VIDEO_URL%

SET VIDEO_URL=https://www.youtube.com/watch?v=G6f0w5BRasw

yt-dlp -o "02-karate-kid-how-jacket-on-off-strengthens.%(ext)s" %VIDEO_URL%
```

The videos prove:

* The power of daily practice - any skill can be developed
* Choose the right coach
  * person - could be
    * friend, teacher, colleague
    * father, mother, brother, sister, relative,...
    * professional trainer
    * expert
  * video tutorial - youtube/paid video courses
  * Books - Evaluate and choose the right book as per the need
  * MOOC courses
    * [Coursera](https://www.coursera.org/)
    * [EDX](https://www.edx.org/)
    * [Freecode camp](https://www.freecodecamp.org/) and [youtube-freecodecamp](https://www.youtube.com/@freecodecamp)
    * [University of Helsinki](https://www.mooc.fi/en/)
    * Other possibilities
* Trust the training and do follow sincerely and obediently. Do daily practice
* Have patience and then validate

## How to download a playlist?

* How to learn excel using the below playlist of videos

```cmd
SET VIDEO_URL=https://www.youtube.com/playlist?list=PLpQQipWcxwt_wKeFEmZL15qOZEkiVUQAq

yt-dlp -o "%(playlist)s/%(playlist_index)s-%(title)s.%(ext)s" %VIDEO_URL%
```

## For audio - download and setup ffmpeg

Refer [ffmpeg setup](ffmpeg.md)

## How to download only audio from youtube video?

* As a man thinketh - by James Allen

```cmd
SET VIDEO_URL=https://www.youtube.com/watch?v=VeBX4WjhhXs
SET FILENAME=as-a-man-thinketh-james-allen

yt-dlp -o "%FILENAME%.mp3" --extract-audio --audio-format mp3 --ffmpeg-location E:\apps\ffmpeg %VIDEO_URL%
```

## Download enire playlist videos and convert to audio - Windows

* Download and listen to the 10 tips that might help everyday life

```cmd
SET PLAYLIST_URL=https://www.youtube.com/watch?list=PLhgOrK0kIYn8v87Rt3THjDQvNy0GPg4RF

yt-dlp -o "%(playlist)s/%(playlist_index)s-%(title)s.%(ext)s"  --extract-audio --audio-format mp3 --ffmpeg-location E:\apps\ffmpeg %PLAYLIST_URL%
```
