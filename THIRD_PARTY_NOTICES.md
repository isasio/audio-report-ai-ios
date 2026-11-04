# Third-party notices

Audio Report AI for iOS includes the following third-party components and model
weights. The full license texts are in [LICENSES](LICENSES).

## LFM3-1.7B QAD Q4_0

- Copyright: Liquid AI, Inc.
- Source: <https://huggingface.co/LiquidAI/LFM3-1.7B-GGUF>
- File: `LFM3-1.7B-QAD-Q4_0.gguf`
- Size: 1,049,615,680 bytes
- SHA-256: `43a7d09a0e9cba91b63eb7052488b9564569bddfd65754d2e426465e572a7452`
- License: LFM Open License v1.0 (see `LICENSES/LFM-Open-License-1.0.txt`)

The LFM Open License includes a commercial-use threshold. Redistribution must
retain the license and attribution. This project does not claim endorsement by
Liquid AI.

## Whisper large-v3-turbo q5_0

- Model weights: OpenAI Whisper, distributed through the whisper.cpp model
  repository.
- Source: <https://huggingface.co/ggerganov/whisper.cpp>
- File: `ggml-large-v3-turbo-q5_0.bin`
- Size: 574,041,195 bytes
- SHA-256: `394221709cd5ad1f40c46e6031ca61bce88931e6e088c188294c6d5a55ffa7e2`
- License: MIT (see `LICENSES/Whisper-MIT.txt`)

## llama.cpp

- Source: <https://github.com/ggml-org/llama.cpp>
- Pinned commit: `1ab23c33b7599e9e73fdcd6584985ae02ce8da83` (b12012)
- License: MIT (see `LICENSES/llama.cpp-MIT.txt`)

## whisper.cpp

- Source: <https://github.com/ggml-org/whisper.cpp>
- Version: v1.8.7
- License: MIT (see `LICENSES/whisper.cpp-MIT.txt`)

## FFmpeg

- Source: <https://github.com/FFmpeg/FFmpeg>
- Version: n8.1.3, commit `1041abdc962f4cc4f394aa8de9dc5236c0c3b9e7`
- Configuration: minimal LGPL build with only the audio decode, resample, and
  filter components required for transcription; no GPL components, no network,
  no programs.
- License: LGPL-2.1-or-later (see `LICENSES/FFmpeg-LGPL-2.1.txt`)

FFmpeg is linked into the iOS app in a static configuration. The corresponding
FFmpeg source is available at the commit above and the build configuration is
documented in [FFMPEG-SOURCE.md](FFMPEG-SOURCE.md). For LGPL relinking
information, open an issue in this repository without including sensitive data.

## Apple frameworks

The app links Apple system frameworks (SwiftUI, SwiftData, AVFoundation, Metal,
and related frameworks) under the iOS SDK terms. They are not redistributed by
this repository.
