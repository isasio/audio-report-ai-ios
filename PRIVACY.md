# Privacy statement

Audio Report AI for iOS is designed to process documentation data locally.

## What the app processes

- Audio recorded with the microphone
- Audio files imported through the system file picker
- Transcripts, including original and corrected text
- Speaker names and roles entered by the user
- Report drafts, versions, evidence links, approval status, and writing modes
- App settings

## Where data goes

The app contains no networking code and no account system. It does not send
audio, transcripts, reports, writing modes, or model data to the developer or to
any third party. There are no analytics, ads, telemetry, remote logging, or
crash-reporting SDKs.

Data stays in the app's private sandbox. It leaves the app only when the user
explicitly exports a transcript or report through the iOS share sheet. The app
or service selected in the share sheet has its own privacy practices.

The bundled LFM3 and Whisper models are included in the app; they are not
downloaded at runtime.

## Permissions

- **Microphone:** used only when the user starts a recording.
- **Files:** the system file picker is used to import audio or text and to
  export files. No broad storage permission is requested.

Permissions can be changed at any time in iOS Settings.

## Retention and deletion

Sessions, audio, transcripts, reports, and exports remain on the device until
the user deletes them. Deleting a session removes its recording, transcript,
report versions, and exports. Uninstalling the app removes all of its data.

## Medical disclaimer

Audio Report AI is a documentation aid, not a medical device. It does not
diagnose, treat, cure, or prevent any condition and does not replace
professional judgement. Reports remain drafts until a qualified person reviews
and explicitly approves them.

## Contact

For privacy questions, open an issue in this repository. Do not include patient
data, recordings, transcripts, or other sensitive information in an issue.
