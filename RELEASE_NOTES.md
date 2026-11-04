# Audio Report AI 0.1.0 — iOS unsigned IPA

Early local-first iOS build with bundled on-device models.

- LFM3-1.7B QAD Q4_0 GGUF for report drafting
- Whisper large-v3-turbo q5_0 for transcription
- FFmpeg audio decode/resample/cleanup pipeline
- Local recording, audio import, transcript review, speaker roles
- Structured report drafts, evidence links, validation, version history, approval
- PDF, JSON, and text export through the system share sheet

## Install

This is an unsigned IPA. You sign it with your own free Apple ID using a
sideloading tool. Sideloadly and AltStore are documented; SideStore is optional.
See [INSTALL.md](INSTALL.md).

Free-Apple-ID installs expire after 7 days and must be refreshed.

## What changed in 0.1.0

- First public iOS build.
- Report output budgets: Short 4k, Normal 8k, Long 12k, Extensive 16k tokens.
- Context scales to 16k, 16k, 24k, and 32k tokens by report length.
- Session deletion from the session detail screen, swipe actions, and Edit mode.
- Delete-all sessions in Settings.
- Session search, stale-status recovery, and improved generation diagnostics.
- Corrected report truncation guidance and Settings budget display.

## Important

- Documentation aid, not a medical device. Reports remain drafts until a human
  reviews and approves them.
- The app is approximately 1.5 GB because both models are bundled.
- App Store and TestFlight distribution are not available for this build; they
  require a paid Apple Developer Program membership.
- LFM3 is redistributed under the LFM Open License v1.0, including its
  commercial-use threshold. See [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).
