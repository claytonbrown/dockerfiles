v4l2rtspserver
==============

[v4l2rtspserver][1] is a RTSP Server for V4L2 device capture supporting HEVC/H264/JPEG/VP8/VP9.

## up and running

```bash
$ v4l2-ctl -d /dev/video0 --list-formats-ext --info
$ docker-compose up -d
$ vlc --network-caching=50 --rtsp-tcp rtsp://127.0.0.1/live
$ ffmpeg -rtsp_transport tcp -i rtsp://127.0.0.1/live -acodec copy -vcodec copy -t 60 cctv.mp4
$ vlc cctv.mp4
```

[1]: https://github.com/mpromonet/v4l2rtspserver
