## Web Video Test

To test, go to https://gabrielssanches.github.io/web-video-test

Also try: https://tools.woolyss.com/html5-audio-video-tester

### Video encoding

This is how video samples were obtained 

#### AV1 [mp4] Orignal file

from: https://github.com/SPBTV/video_av1_samples/blob/master/spbtv_sample_bipbop_av1_960x540_25fps.mp4 -> video-av1.mp4

#### H.263 [mp4]

```shell
ffmpeg -i video-av1.mp4 -vf scale=1408:1152 -c:v h263 -qscale:v 10 -c:a aac -b:a 64k video-h263.3gp
```

#### H.263 [3gp]

```shell
ffmpeg -i video-av1.mp4 -vf scale=1408:1152 -c:v h263 -qscale:v 10 -c:a aac -b:a 64k video-h263.3gp
```

#### HEVC (H.265) [mp4]

```shell
ffmpeg -i video-av1.mp4 -c:v libx265 -crf 28 -preset medium video-hevc-h265.mp4
```

#### MP4V-ES (MPEG-4 Visual) [mp4]

```shell
ffmpeg -i video-av1.mp4 -c:v mpeg4 -qscale:v 2 video-mp4v-es.mp4
```

#### MPEG-1 [mpg]

```shell
ffmpeg -i video-av1.mp4 -c:v mpeg1video -qscale:v 2 video-mpeg1.mpg
```

#### MPEG-2 [mpg]

```shell
ffmpeg -i video-av1.mp4 -c:v mpeg2video -qscale:v 2 video-mpeg2.mpg
```

#### Theora [ogv]

```shell
ffmpeg -i video-av1.mp4 -c:v libtheora -qscale:v 7 video-theora.ogv
```

#### VP8 [webm]

```shell
ffmpeg -i video-av1.mp4 -c:v libvpx -b:v 1M video-vp8.webm
```

#### VP9 [webm]

```shell
ffmpeg -i video-av1.mp4 -c:v libvpx-vp9 -b:v 1M video-vp9.webm
```
