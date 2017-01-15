# avconv cheat sheet

### Crop video (based on start and length)
```sh
avconv -i INPUT.mp4 -acodec copy -vcodec copy -ss 00:15:00 -t 00:00:10 OUTPUT.mp4
```

### Merge video and audio
```sh
avconv -i INPUT_VIDEO.mp4 -i INPUT_AUDIO.mp3 -codec copy -shortest OUTPUT.mp4
```

### Convert stereo to mono
```sh
avconv -i INPUT.mp3 -ac 1 OUTPUT.mp3
```

### Get audio track from video
```sh
avconv -i INPUT.mp4 -acodec libmp3lame -ac 2 -ab 128k -vn -y OUTPUT.mp3
```

### Remove audio track from video
```sh
avconv -i INPUT.mp4 -vcodec copy -an OUTPUT.mp4
```
### Rotave video
```sh
avconv -i INPUT.mov -vf transpose=1 -strict -2 OUTPUT.mov

# For the transpose parameter you can pass:
# 0 = 90CounterCLockwise and Vertical Flip (default) 
# 1 = 90Clockwise 
# 2 = 90CounterClockwise 
# 3 = 90Clockwise and Vertical Flip
```

### Convert to GIF
```sh
avconv -ss 00:00:00.000 -i INPUT.mov -pix_fmt rgb24 -r 10 -s 640x320 OUTPUT.gif
```
