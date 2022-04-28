Merge video and audio:

> ffmpeg -i video.mp4 -i audio.wav -c:v copy -c:a aac -strict experimental output.mp4
> or
> ffmpeg -i video.mp4 -i audio.wav -c copy output.mkv

Split video by timestamp:

> ffmpeg -ss 00:00:00 -t 00:50:00 -i largefile.mp4 smallfile.mp4

Merge videos:

> ffmpeg -f concat -safe 0 -i fileList.txt merged.mp4

Compress video, crf = 0 lossless, 50 supercompressed, 21 default:

> ffmpeg -i input.mp4 -threads 4 -vcodec libx265 -crf 28 -preset veryfast compressed.mp4
