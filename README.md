# avconv cheat sheet

## Cropping the video based on start and length

```bash
avconv -i INPUT.mp4 -acodec copy -vcodec copy -ss 00:15:00 -t 00:00:10 OUTPUT.mp4
```

