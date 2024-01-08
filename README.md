# ffmpeg-avfoundation
FFmpeg has a bug in Mac avfoundation audio capturing somewhere at or after v4.3 up to today's v6.1.1 in 2024 

After compiling FFmpeg v4.2.3 for Mac Arm64, recording or streaming is not longer choppy. 

```bash
/opt/homebrew/Cellar/ffmpeg/4.2.3/bin/ffmpeg -f avfoundation \
          -i ":BlackHole 16ch" \
          -acodec eac3 \
          -ab 640k \
          -ac 6 \
          -f rtp_mpegts rtp://192.168.0.173:1234
```
