# Installing Audio Report AI on iPhone or iPad

This build is **unsigned**. iOS will not install it directly. You sign it with
your own free Apple ID using a sideloading tool.

You can use any free tool that supports unsigned IPA installation. The
instructions below cover the common options. You do **not** have to install
SideStore.

## Before you start

- iOS 18 or newer on an iPhone or iPad.
- About 3 GB free storage.
- A free Apple ID. You do not need a paid Apple Developer Program membership.
- The latest `AudioReportAI-unsigned.ipa` from the
  [releases page](https://github.com/isasio/audio-report-ai-ios/releases/latest).
- Optional: verify the checksum before installing:

```bash
shasum -a 256 -c AudioReportAI-unsigned.ipa.sha256
```

## Option A — Sideloadly (Windows or macOS, USB)

This is the shortest first-install path.

1. Download and install [Sideloadly](https://sideloadly.io/).
2. Connect the iPhone or iPad by USB, unlock it, and trust the computer.
3. Open Sideloadly and drag `AudioReportAI-unsigned.ipa` into the IPA field.
4. Enter your Apple ID. The credentials go only to Sideloadly and Apple's
   signing service on your computer; they are never sent to this project.
5. Click **Start**. Enter the Apple ID password or app-specific password when
   prompted, and complete two-factor authentication if asked.
6. On the device, open **Settings → General → VPN & Device Management**, select
   your Apple ID developer certificate, and tap **Trust**.
7. Open **Settings → Privacy & Security → Developer Mode**, turn it on, and
   restart the device if prompted.
8. Open Audio Report AI.

## Option B — AltStore (Windows or macOS, Wi-Fi refresh)

AltStore is a good choice if you want to refresh without a cable later.

1. Install **AltServer** from [altstore.io](https://altstore.io/) on a Windows
   or macOS computer on the same Wi-Fi network as the device.
2. Connect the device by USB once and install AltStore through AltServer.
3. On the device, trust your Apple ID certificate in
   **Settings → General → VPN & Device Management**.
4. Enable **Developer Mode** in **Settings → Privacy & Security** and restart.
5. Open AltStore, sign in with the same Apple ID, and go to **My Apps → +**.
6. Select the downloaded IPA and let AltStore sign and install it.
7. Keep AltServer running on the computer when you need to refresh.

## Option C — SideStore (optional, Wi-Fi refresh)

SideStore is optional. It is useful if you want to refresh over Wi-Fi without
keeping a computer running AltServer. It requires a one-time setup with a
computer and a pairing file.

Follow the official SideStore documentation for your operating system:

- <https://sidestore.io/>

After setup, open SideStore → **My Apps → +**, select the IPA, and let SideStore
sign it with your Apple ID. LocalDevVPN must be connected when SideStore installs
or refreshes apps.

## The 7-day limit

A free Apple ID signs apps for **7 days**. When the app expires:

- It may stop opening until it is refreshed.
- Open your sideloading tool and refresh/reinstall the app.
- Your sessions and reports are preserved when you refresh the same app; they
  are removed if you uninstall the app or change its bundle identifier.

A free Apple ID also has a small limit on how many sideloaded apps can be active
at once. Remove unused sideloaded apps if installation fails.

## Troubleshooting

- **"Untrusted Developer"**: trust the Apple ID certificate in
  **Settings → General → VPN & Device Management**.
- **"Developer Mode required"**: enable it in
  **Settings → Privacy & Security → Developer Mode**, then restart.
- **Install fails**: confirm the device is unlocked, the IPA is the device build
  (not a simulator build), and your signing tool is up to date.
- **App expires after a week**: refresh it with the same tool before the 7-day
  counter reaches zero.
- **SideStore cannot install**: confirm LocalDevVPN is connected and SideStore
  itself has not expired.
- **Out of storage**: the IPA is about 1.5 GB; keep at least 3 GB free during
  installation.

## Privacy and credentials

Apple ID credentials are handled by the sideloading tool on your computer or
device. Never send your Apple ID password, signing certificate, or `.p8` key to
this project or put it in a GitHub issue.
