# FFmpeg source and LGPL information

Audio Report AI uses a minimal FFmpeg build for local audio decode, resampling,
and cleanup before Whisper transcription.

## Exact source

- Project: FFmpeg
- Version: n8.1.3
- Commit: `1041abdc962f4cc4f394aa8de9dc5236c0c3b9e7`
- Source: <https://github.com/FFmpeg/FFmpeg/tree/1041abdc962f4cc4f394aa8de9dc5236c0c3b9e7>
- License: LGPL-2.1-or-later

## Build configuration

The build is intentionally minimal and contains no GPL components, no network
support, and no FFmpeg command-line programs.

```text
--disable-everything
--disable-autodetect
--disable-programs
--disable-doc
--disable-network
--disable-avdevice
--disable-swscale
--disable-asm
--disable-zlib
--disable-bzlib
--disable-lzma
--disable-iconv
--disable-xlib
--disable-libdrm
--disable-vdpau
--disable-vaapi
--disable-v4l2-m2m
--enable-avformat
--enable-avcodec
--enable-avfilter
--enable-swresample
--enable-protocol=file
--enable-demuxer=wav,mov,mp3,aac,caf,flac,ogg,matroska,aiff
--enable-decoder=pcm_s16le,pcm_s24le,pcm_s32le,pcm_f32le,pcm_f64le,pcm_s16be,pcm_s24be,pcm_s32be,pcm_u8,pcm_alaw,pcm_mulaw,aac,mp3,alac,flac,vorbis,opus
--enable-parser=aac,mpegaudio,flac,vorbis,opus
--enable-filter=anull,aresample,aformat,highpass,lowpass,afftdn,loudnorm,volume
--enable-static
--disable-shared
--disable-symver
--disable-debug
```

## LGPL relinking

FFmpeg is statically linked into the iOS app. If you need the relinking
materials required by LGPL-2.1 section 6, open an issue in this repository and
describe the materials you need. Do not include personal data, audio,
transcripts, or reports in the issue.

The goal is to provide the corresponding FFmpeg source access and the
object-code/relinking materials needed to exercise your LGPL rights without
exposing user data or signing credentials.
