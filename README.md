# Audio Report AI for iOS

<img src="Assets/icon.png" width="96" alt="Audio Report AI app icon">

A local-first iOS app for recording or importing conversations, transcribing
them on-device, reviewing the transcript, and drafting structured reports with a
local LFM3 model.

**No cloud. No account. No runtime networking.**

## Download

**[Download the latest unsigned IPA](https://github.com/isasio/audio-report-ai-ios/releases/latest/download/AudioReportAI-unsigned.ipa)**

- Version: **0.1.0**
- Size: **~1.5 GB**
- iOS 18 or newer
- iPhone and iPad
- SHA-256: see `SHA256SUMS.txt` on the latest release

## Installation

iOS requires every app to be signed. This build is unsigned, so it must be
signed with your own free Apple ID using a sideloading tool.

You do **not** have to use SideStore. Any of these free options works:

- **Sideloadly** (Windows or macOS, USB cable) — simplest first install.
- **AltStore** (Windows or macOS, one-time setup) — installs and refreshes over
  Wi-Fi.
- **SideStore** (optional) — a Wi-Fi refresh workflow after a one-time setup.

A free Apple ID can install apps for **7 days at a time**. Refresh the app before
it expires. A paid Apple Developer Program membership is required for TestFlight
or the App Store, so those are not available for this build.

### Why not the App Store?

Publishing to the App Store requires the paid Apple Developer Program
membership (currently $99/year). The app itself is free: there is no purchase,
subscription, ad, or account. Until a membership exists, this repository
distributes the unsigned IPA so anyone with a free Apple ID can install it.
If this is a nonprofit, educational, or government project, Apple may consider a
Developer Program fee waiver.

See [INSTALL.md](INSTALL.md) for step-by-step instructions and troubleshooting.

## What it does

- Records audio locally, or imports audio from Files
- Cleans and resamples audio on-device with FFmpeg
- Transcribes with the bundled Whisper large-v3-turbo model through
  whisper.cpp/Metal
- Preserves raw and corrected transcript text separately
- Supports manual speaker names and roles
- Drafts structured reports with the bundled LFM3-1.7B model through
  llama.cpp/Metal
- Links report statements to transcript evidence
- Keeps reports as drafts until a human explicitly approves them
- Supports short, normal, long, and extensive report lengths
- Includes reusable writing modes, a linter, prompt preview, and version history
- Exports transcripts and reports as PDF, JSON, or text through the system share
  sheet

## Bundled models

| Model | Purpose | Approx. size |
| --- | --- | --- |
| LFM3-1.7B QAD Q4_0 GGUF | Report drafting | 1.05 GB |
| Whisper large-v3-turbo q5_0 | Transcription | 574 MB |

The models are bundled with the app. Nothing is downloaded at runtime.

## Privacy

- No account, ads, analytics, telemetry, remote logging, or crash-reporting SDK.
- The app contains no networking code.
- Audio, transcripts, reports, modes, and models stay in the app sandbox.
- Data leaves the app only when you explicitly export it through the system
  share sheet.
- Deleting a session removes its audio, transcript, report versions, and
  exports from the device.

See [PRIVACY.md](PRIVACY.md) for details.

## Requirements

- iPhone or iPad running iOS 18 or newer
- About 3 GB free storage for the app and its bundled models
- A free Apple ID and a sideloading tool for installation
- A Wi-Fi connection for the initial download; the app itself works offline

## Important limitations

Audio Report AI is a **documentation aid, not a medical device**. It does not
diagnose, treat, cure, or prevent any condition and does not replace
professional judgement. Generated reports are drafts and must be reviewed,
corrected, and explicitly approved by a qualified person before use.

This is a **0.1.0 early build**:

- Free-Apple-ID installs expire after 7 days and must be refreshed.
- App Store and TestFlight distribution are not available for this build.
- Report generation can take several minutes on a phone, especially Extensive.
- The app is English-language UI; report and transcript languages include
  Spanish, English, Portuguese, French, German, Italian, and automatic.

## Licenses

The app includes model and third-party license texts in Settings and in the app
bundle. See:

- [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md)
- [FFMPEG-SOURCE.md](FFMPEG-SOURCE.md)
- [LICENSES](LICENSES)

The LFM3 model is redistributed under the **LFM Open License v1.0**, including
its commercial-use threshold. Whisper, llama.cpp, and whisper.cpp are
MIT-licensed. FFmpeg is used in an LGPL-2.1-or-later configuration. This
repository does not claim endorsement by Liquid AI or OpenAI.

## About this repository

This public repository distributes the unsigned iOS build and its user-facing
documentation. Source code, signing certificates, and model files are not stored
here. The IPA and checksums are published as GitHub Release assets.

For support, open an issue in this repository.
