List all available formats:
> pytube <LINK> --list

Download 1080p 30fps:
> pytube <LINK> --itag=137

Download 1080p 60fps:
> pytube <LINK> --itag=299

Download audio:
> pytube <LINK> --itag=140

Merge:
> ffmpeg -i video.mp4 -i audio.wav -c:v copy -c:a aac -strict experimental output.mp4
> or
> ffmpeg -i video.mp4 -i audio.wav -c copy output.mkv
