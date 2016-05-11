# avconv cheat sheet

### Cropping the video based on start and length
```bash
avconv -i INPUT.mp4 -acodec copy -vcodec copy -ss 00:15:00 -t 00:00:10 OUTPUT.mp4
```

### Merge video and audio
```bash
avconv -i INPUT_VIDEO.mp4 -i INPUT_AUDIO.mp3 -codec copy -shortest OUTPUT.mp4
```

### Convert stereo to mono
```bash
avconv -i INPUT.mp3 -ac 1 OUTPUT.mp3
```

### Get audio track from video
```bash
avconv -i INPUT.mp4 -acodec libmp3lame -ac 2 -ab 128k -vn -y OUTPUT.mp3
```
